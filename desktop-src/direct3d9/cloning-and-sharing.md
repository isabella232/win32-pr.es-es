---
description: Clonación y uso compartido (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonación y uso compartido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907481"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonación y uso compartido (Direct3D 9)

## <a name="cloning-parameters"></a>Parámetros de clonación

La clonación tiene las siguientes restricciones.

-   Los clones heredan el grupo del efecto original. Vea la sección parámetros de uso compartido.
-   Los clones heredan las técnicas, las pasadas, los parámetros y las anotaciones del efecto original (incluidas todas las anotaciones agregadas con [**ID3DXEffect**](id3dxeffect.md)).
-   Los clones heredan las anotaciones agregadas dinámicamente del efecto original.
-   La clonación en un nuevo dispositivo producirá un error si el grupo del efecto original no era **nulo** y el efecto original contenía un parámetro dependiente del dispositivo compartido (como una textura o un sombreador).

## <a name="sharing-parameters"></a>Parámetros de uso compartido

Un grupo es un búfer que comparte parámetros de efectos entre distintos efectos. Para agregar parámetros a un grupo, especifique un uso compartido cuando se cree el efecto.

Un grupo tiene las restricciones siguientes.

-   Un parámetro se agrega al grupo la primera vez que se agrega al grupo un efecto que contiene el parámetro (compartido).
-   Un grupo obtiene los valores iniciales del primer parámetro compartido; los parámetros compartidos posteriormente obtienen sus valores del grupo.
-   Un parámetro se elimina del grupo cuando se liberan todas las referencias de efecto al parámetro compartido.
-   Todos los efectos del grupo que contengan el mismo parámetro dependiente del dispositivo (compartido) deben tener el mismo dispositivo.

**Null** se puede usar para especificar ningún grupo, en cuyo caso no se comparte ningún parámetro. Esto es casi equivalente a especificar un grupo único solo para este efecto. La única diferencia es que, cuando se clona el efecto, el clon no compartirá sus parámetros compartidos con el original.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



