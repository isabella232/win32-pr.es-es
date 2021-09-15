---
description: La validación se realiza durante la compilación del efecto. Para validar la técnica actual, especifique NULL como identificador de técnica que se va a validar.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580125"
---
# <a name="validation-direct3d-9"></a>Validación (Direct3D 9)

La validación se realiza durante la compilación del efecto. Para validar la técnica actual, especifique **NULL como** identificador de técnica que se va a validar.

Se producirá un error en la validación para cualquiera de las siguientes opciones:

-   Si el identificador de técnica especificado no existe.
-   Si se produce un error en la aplicación de cualquier estado en cualquier paso de la técnica.
-   Si se produce un error en la validación del dispositivo después de la aplicación de todos los estados en cualquier paso de la técnica.
-   Si a los estados de efecto PIXELSHADER o VERTEXSHADER se les asignan sombreadores no válidos en cualquier paso de la técnica.
-   Si los límites del dispositivo no admiten la asignación de cubos y se asigna un estado de efecto TEXTURE a un valor de tipo textureCUBE en cualquier paso de la técnica.
-   Si los límites de dispositivo no admiten la asignación de volúmenes y se asigna un estado de efecto TEXTURE a un valor de tipo texture3D en cualquier paso de la técnica.

Para obtener más información, [vea Estados de efecto (Direct3D 9).](effect-states.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



