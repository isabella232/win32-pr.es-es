---
description: Estas constantes se aplican a las variables de efecto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Constantes de D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705282"
---
# <a name="d3d10_effect_variable-constants"></a>Constantes de variable de \_ efecto de D3D10 \_

Estas constantes se aplican a las variables de efecto.



| \#define                                       | Descripción  | Value                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ \_ anotación de variable de efecto \_            | 1 << 0 | Indica que se trata de una anotación o una variable global.                                                                                                                                                                                                        |
| \_Variable de efecto D3D10 \_ \_ agrupada                | 1 << 1 | Indica que esta variable o búfer de constantes reside en un grupo de efectos. Si no se establece esta marca, la variable se encuentra en un efecto independiente o en un efecto secundario (los efectos independientes devuelven false desde [**ID3D10Effect:: IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)). |
| \_Punto de \_ \_ enlace explícito \_ de variable de efecto de \_ D3D10 | 1 << 2 | Indica que la variable se ha enlazado explícitamente mediante la palabra clave Register.                                                                                                                                                                                 |



 

Estas marcas se definen como macros en d3d10effect. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



