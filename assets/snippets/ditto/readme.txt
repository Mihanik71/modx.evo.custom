
Andchir

http://modx-shopkeeper.ru

-----------------------------------------

��������� ����������� � ��������� &where �������� ������� ������� (SQL) �� TV (�� ������ ���� �������� ������ ������� ������ �� ������� "content"). ����� �������� "mode" - 12 ��� ���������� �� ������������� ��������� ����� (��������� ��� TV) � ������� "���".

-----------------------------------------

������:

[[Ditto? &tpl=`dittoChunk`&where=`@SQL: AND (tvc.tmplvarid = '10' AND tvc.value @eq '��������')`]]

�.�. ��� �������������� ������� ��� ������� �� �� �� ID TV (tvc.tmplvarid) � ��� �������� (tvc.value).
@eq - ��� "�����" (=). @eq ����� ������ ��� ������ �������� � �������, �.�. ������ �� ��������� ���������� "=". ��� ������ � PHP ����� ����� � ������ ������ "=", �.�.:

$modx->runSnippet('Ditto', array(
  "tpl" => "dittoChunk",
  "where" => "@SQL: AND (tvc.tmplvarid = '10' AND tvc.value = '��������')"
));

��� ������� ��� �������������, �.�. ��� &filter ���������� ���������� ������ ����� ���� ��� ��� ��������� (�� ��������) �������� �� ����. ��� ����� ���� �������� �������, ���� ���������� ����� �����.

-----------------------------------------

������ ����������:


[[Ditto? &filter=`tvname,������~�����~�������,12`]]

��������� ������ ���������, � ������� � ��������� TV � ������ "tvname" ���� ��������� ��������, ����������� "~" (��������� �������������).

