---
description: Estas constantes se usan al crear un efecto para definir el comportamiento de compilación o el comportamiento del efecto en tiempo de ejecución.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3738a95a843020f7c0f8af30e8c5d035f0a86ac7098d36cae422eb01ed4dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736054"
---
# <a name="d3d10_effect-constants"></a>D3D10 \_ EFFECT (Constantes)

Estas constantes se usan al crear un efecto para definir el comportamiento de compilación o el comportamiento del efecto en tiempo de ejecución.



| \#Definir                                 | Value        | Descripción                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EFECTO D3D10 \_ EFECTO \_ SECUNDARIO DE \_ \_ COMPILACIÓN    | 1 << 0 | Compile el archivo .fx en un efecto secundario. Los efectos secundarios no tienen inicializaciones para ningún valor compartido porque se inicializan en el grupo de efectos.                                                                                                           |
| COMPILACIÓN DE EFECTO D3D10 \_ \_ PERMITIR OPERACIONES \_ \_ \_ LENTAS | 1 << 1 | De forma predeterminada, el modo de rendimiento está habilitado. El modo de rendimiento no permite objetos de estado mutable evitando que las expresiones no literales aparezcan en las definiciones de objetos de estado. Si se especifica esta marca, se deshabilitará el modo y se permitirán objetos de estado mutable. |
| EFECTO D3D10 \_ \_ CON SUBPROCESO \_ ÚNICO          | 1 << 3 | No intente sincronizar con otros subprocesos cargando efectos en el mismo grupo.                                                                                                                                                                        |



 

Estas constantes se definen como macros en d3d10effect.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



