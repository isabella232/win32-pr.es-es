---
title: Propiedad Application.Views
description: Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la cinta de opciones y contextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Cinta de opciones de la Windows Application.Views
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe063397698a74da0421cf0c9c3b2ef46861f1477e0f4ac99fe5d6e6063c7251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964314"
---
# <a name="applicationviews-property"></a>Propiedad Application.Views

Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la [**cinta de opciones**](windowsribbon-element-ribbon.md) y [**contextPopup**](windowsribbon-element-contextpopup.md).

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
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/>             | Debe producirse exactamente una vez<br/> <br/>     |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Aplicación**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Comentarios

Obligatorio.

Debe producirse exactamente una vez para cada [**elemento Application.**](windowsribbon-element-application.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un **elemento Application.Views** que contiene un manifiesto de controles Ribbon, cada uno con una referencia a un comando declarado en el [**elemento Application.Commands.**](windowsribbon-element-application-commands.md)


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Application.Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





