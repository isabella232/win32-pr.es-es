---
title: UI_PKEY_TooltipDescription
description: Identifica la propiedad TooltipDescription de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900610c1302d3cc904dcde2d7c86801982fd4d10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676265"
---
# <a name="ui_pkey_tooltipdescription"></a>UI \_ PKEY \_ TooltipDescription

Identifica la propiedad TooltipDescription de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY TooltipDescription para consultar la descripción asociada a una [interfaz de usuario \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md).

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.

 

La longitud máxima del TooltipDescription de PKEY de la interfaz de usuario \_ \_ no está enlazada.

No se admite la alineación derecha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de recursos](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




