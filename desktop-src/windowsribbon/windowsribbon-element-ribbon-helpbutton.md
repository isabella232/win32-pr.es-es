---
title: Propiedad Ribbon. HelpButton
description: Representa un contenedor para el botón ayuda.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Ribbon. HelpButton (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802870"
---
# <a name="ribbonhelpbutton-property"></a>Propiedad Ribbon. HelpButton

Representa un contenedor para el [botón ayuda](windowsribbon-controls-helpbutton.md).

## <a name="usage"></a>Uso

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                           | Descripción                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico necesario para implementar un botón de ayuda de la cinta de opciones.

En esta sección de código se muestra la declaración de comando **Ribbon. HelpButton** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



En esta sección de código se muestra la declaración de control **Ribbon. HelpButton** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





