---
title: Elemento Ribbon
description: Representa el control de la cinta de opciones en la vista de la cinta.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Cinta de opciones de Windows (elemento)
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714279"
---
# <a name="ribbon-element"></a>Elemento Ribbon

Representa el control de la cinta de opciones en la vista de la cinta.

## <a name="usage"></a>Uso

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
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
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> Pequeño<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> Medio<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Amplíe<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nombre</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Se utiliza para anotar el elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cualquier secuencia de cero o más caracteres.<br/> La longitud máxima es sin límite.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                         | Descripción                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Puede aparecer como máximo una vez<br/> <br/> |
| [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Puede aparecer como máximo una vez<br/> <br/> |
| [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Puede aparecer como máximo una vez<br/> <br/> |
| [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |
| [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Puede aparecer como máximo una vez<br/> <br/> |
| [**Cinta. pestañas**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez para cada elemento [**Application. views**](windowsribbon-element-application-views.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico de una vista de **la cinta** de opciones.


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



 

 





