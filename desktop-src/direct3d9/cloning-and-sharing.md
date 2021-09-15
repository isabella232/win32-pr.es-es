---
description: Clonación y uso compartido (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonación y uso compartido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566665"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonación y uso compartido (Direct3D 9)

## <a name="cloning-parameters"></a>Clonación de parámetros

La clonación tiene las restricciones siguientes.

-   Los clones heredan el grupo del efecto original. Consulte la sección Parámetros de uso compartido.
-   Los clones heredan las técnicas, los pases, los parámetros y las anotaciones del efecto original (incluidas todas las anotaciones agregadas [**con ID3DXEffect).**](id3dxeffect.md)
-   Los clones heredan las anotaciones agregadas dinámicamente del efecto original.
-   La clonación en un nuevo dispositivo producirá un error si el grupo del efecto original no era **NULL** y el efecto original contenía un parámetro compartido dependiente del dispositivo (por ejemplo, una textura o un sombreador).

## <a name="sharing-parameters"></a>Parámetros de uso compartido

Un grupo es un búfer que comparte parámetros de efecto entre distintos efectos. Para agregar parámetros a un grupo, especifique un uso compartido cuando se cree el efecto.

Un grupo tiene las restricciones siguientes.

-   La primera vez que se agrega un parámetro (compartido) al grupo, se agrega un parámetro al grupo.
-   Un grupo obtiene los valores iniciales del primer parámetro compartido; Los parámetros compartidos posteriormente obtienen sus valores del grupo.
-   Un parámetro se elimina del grupo cuando se liberan todas las referencias de efecto al parámetro compartido.
-   Todos los efectos del grupo que contienen el mismo parámetro dependiente del dispositivo (compartido) deben tener el mismo dispositivo.

**NULL** se puede usar para especificar ningún grupo, en cuyo caso no se comparte ningún parámetro. Esto es casi equivalente a especificar un grupo único solo para este efecto. La única diferencia es que cuando se clona el efecto, el clon no compartirá sus parámetros compartidos con el original.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



