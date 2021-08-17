---
description: Estas constantes se aplican a las variables de efecto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736076"
---
# <a name="d3d10_effect_variable-constants"></a>Constantes DE VARIABLE \_ DE EFECTO D3D10 \_

Estas constantes se aplican a las variables de efecto.



| \#Definir                                       | Descripción  | Value                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ANOTACIÓN DE \_ VARIABLE DE EFECTO D3D10 \_ \_            | 1 << 0 | Indica que se trata de una anotación o una variable global.                                                                                                                                                                                                        |
| VARIABLE DE EFECTO D3D10 \_ \_ \_ AGRUPADA                | 1 << 1 | Indica que esta variable o búfer constante reside en un grupo de efectos. Si no se establece esta marca, la variable reside en un efecto independiente o en un efecto secundario (los efectos independientes devuelven false desde [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool). |
| PUNTO DE ENLACE EXPLÍCITO DE \_ LA VARIABLE DE \_ EFECTO \_ \_ \_ D3D10 | 1 << 2 | Indica que la variable se ha enlazado explícitamente mediante la palabra clave register.                                                                                                                                                                                 |



 

Estas marcas se definen como macros en d3d10effect.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



