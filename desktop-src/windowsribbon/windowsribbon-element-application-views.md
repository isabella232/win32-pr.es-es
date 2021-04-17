---
title: Application. views (propiedad)
description: Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la cinta de opciones y el ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Propiedad Application. views (cinta) de Windows
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705145"
---
# <a name="applicationviews-property"></a>Application. views (propiedad)

Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la [**cinta**](windowsribbon-element-ribbon.md) de opciones y el [**ContextPopup**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Uso

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Descripción                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Puede producirse una o varias veces<br/> <br/> |
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/>             | Debe aparecer exactamente una vez<br/> <br/>     |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Aplicación**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez para cada elemento de la [**aplicación**](windowsribbon-element-application.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un elemento **Application. views** que contiene un manifiesto de controles de la cinta de opciones, cada uno con una referencia a un comando declarado en el elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Application. Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





