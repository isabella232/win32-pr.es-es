---
title: Elemento Ribbon
description: Representa el control de la cinta de opciones en la vista de cinta de opciones.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Cinta de opciones de Windows, elemento
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445006"
---
# <a name="ribbon-element"></a>Elemento Ribbon

Representa el control de la cinta de opciones en la vista de cinta de opciones.

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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (Pequeño)<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> (Medio)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nombre</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Se usa para anotar el elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cualquier secuencia de cero o más caracteres.<br/> La longitud máxima es sin enlazar.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                         | Descripción                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Puede producirse como máximo una vez<br/> <br/> |
| [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Puede producirse como máximo una vez<br/> <br/> |
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Puede producirse como máximo una vez<br/> <br/> |
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Puede producirse como máximo una vez<br/> <br/> |
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application.Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Debe producirse exactamente una vez para [**cada elemento Application.Views.**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para una vista **de cinta** de opciones.


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




* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



 

 





