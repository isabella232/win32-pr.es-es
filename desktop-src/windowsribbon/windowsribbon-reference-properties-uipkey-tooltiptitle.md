---
title: UI_PKEY_TooltipTitle
description: Identifica la propiedad \_ PKEY TooltipTitle de la interfaz \_ de usuario.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437790"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ TooltipTitle

Identifica la propiedad \_ PKEY TooltipTitle de la interfaz \_ de usuario.

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentarios

La interfaz de usuario PKEY TooltipTitle la usa una aplicación para consultar la información sobre herramientas de \_ pestañas, grupos, botones, elementos de la galería y otros controles \_ de la cinta de opciones.

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML de juego de caracteres universales (UCS) `&#xA;` para especificar un salto de línea.

 

No se admite la alineación derecha.

La longitud máxima de PKEY TooltipTitle de la interfaz de \_ \_ usuario es sin enlazar.

Para mostrar una y comercial en una información sobre herramientas, escape la designación de caracteres especiales con una y comercial doble ( ) como se muestra `&&` en el ejemplo siguiente.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




