---
title: Elemento ApplicationMenu
description: Representa el menú de la aplicación. | Elemento ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Elemento ApplicationMenu de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443056"
---
# <a name="applicationmenu-element"></a>Elemento ApplicationMenu

Representa el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                             | Descripción                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> | Puede producirse como máximo una vez<br/> <br/>      |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                     | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse exactamente una vez para [**cada Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).

Los elementos secundarios del **elemento ApplicationMenu** deben producirse en el orden especificado:

1.  [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)
2.  [**MenuGroup**](windowsribbon-element-menugroup.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).

En esta sección de código se muestran las declaraciones del comando **ApplicationMenu.**


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



En esta sección de código se muestran las declaraciones del control **ApplicationMenu.**


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control Menú de la aplicación](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





