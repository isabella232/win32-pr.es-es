---
title: Propiedad Ribbon.Tabs
description: Representa un contenedor para todas las pestañas principales de una cinta de opciones.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Cinta de opciones de la propiedad Ribbon.Tabs Windows cinta de opciones
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574372"
---
# <a name="ribbontabs-property"></a>Propiedad Ribbon.Tabs

Representa un contenedor para todas las pestañas principales de una cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                             | Descripción                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Pestaña**](windowsribbon-element-tab.md)<br/> | Debe producirse al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Observaciones

Necesario.

Puede producirse una o varias veces para cada cinta [**de opciones.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para un **elemento Ribbon.Tabs** con una **declaración De inicio.** [](windowsribbon-element-tab.md)


```C++
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
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





