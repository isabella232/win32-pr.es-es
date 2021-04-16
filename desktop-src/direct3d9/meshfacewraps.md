---
description: Se usa para definir la topología de textura de cada una de las caras de un ajuste. El valor del miembro nFaceWrapValues debe ser igual al número de caras de una malla.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536514"
---
# <a name="meshfacewraps"></a><span data-ttu-id="0d6bb-104">MeshFaceWraps</span><span class="sxs-lookup"><span data-stu-id="0d6bb-104">MeshFaceWraps</span></span>

<span data-ttu-id="0d6bb-105">Se usa para definir la topología de textura de cada una de las caras de un ajuste.</span><span class="sxs-lookup"><span data-stu-id="0d6bb-105">Used to define the texture topology of each face in a wrap.</span></span> <span data-ttu-id="0d6bb-106">El valor del miembro nFaceWrapValues debe ser igual al número de caras de una malla.</span><span class="sxs-lookup"><span data-stu-id="0d6bb-106">The value of the nFaceWrapValues member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

<span data-ttu-id="0d6bb-107">Esta plantilla ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="0d6bb-107">This template is no longer used.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d6bb-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d6bb-108">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d6bb-109">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="0d6bb-109">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



