---
description: Estas constantes se utilizan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Constantes de D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360031"
---
# <a name="d3d10_effect-constants"></a>Constantes de efecto de D3D10 \_

Estas constantes se utilizan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.



| \#define                                 | Value        | Descripción                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Efecto D3D10 \_ compilar \_ \_ efecto secundario    | 1 << 0 | Compile el archivo. FX en un efecto secundario. Los efectos secundarios no tienen ninguna inicialización para los valores compartidos porque se inicializan en el grupo de efectos.                                                                                                           |
| D3D10 \_ efecto \_ compilar \_ permitir \_ operaciones lentas \_ | 1 << 1 | De forma predeterminada, el modo de rendimiento está habilitado. El modo de rendimiento no permite objetos de estado mutable impidiendo que las expresiones no literales aparezcan en las definiciones de objeto de estado. Si se especifica esta marca, se deshabilitará el modo y se permitirán los objetos de estado mutable. |
| Efecto de D3D10 con \_ \_ un único \_ subproceso          | 1 << 3 | No intente sincronizar con otros efectos de carga de subprocesos en el mismo grupo.                                                                                                                                                                        |



 

Estas constantes se definen como macros en d3d10effect. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



