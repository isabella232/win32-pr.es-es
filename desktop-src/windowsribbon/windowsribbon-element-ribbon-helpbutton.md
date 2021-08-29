---
title: Propiedad Ribbon.HelpButton
description: Representa un contenedor para el botón ayuda.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Cinta de opciones de la propiedad Ribbon.HelpButton Windows cinta de opciones
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba568fcd18ab16e1c8bd878dc786b2c415a0329d1bd430e78ec9b03a73424df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933204"
---
# <a name="ribbonhelpbutton-property"></a>Propiedad Ribbon.HelpButton

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
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada cinta [**de opciones.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico necesario para implementar un botón Ayuda de la cinta de opciones.

En esta sección de código se muestra la declaración del comando **Ribbon.HelpButton.**


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



En esta sección de código se muestra la declaración de control **Ribbon.HelpButton.**


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





