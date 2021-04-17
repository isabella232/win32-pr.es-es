---
title: UI_PKEY_TooltipTitle
description: Identifica la propiedad TooltipTitle de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704729"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ TooltipTitle

Identifica la propiedad TooltipTitle de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY TooltipTitle para consultar la información sobre herramientas, grupos, botones, elementos de la galería y otros controles de la cinta de opciones.

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.

 

No se admite la alineación derecha.

La longitud máxima del TooltipTitle de PKEY de la interfaz de usuario \_ \_ no está enlazada.

Para mostrar una y comercial en una información sobre herramientas, escape la designación de carácter especial con un signo de y comercial ( `&&` ) como se muestra en el ejemplo siguiente.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de recursos](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




