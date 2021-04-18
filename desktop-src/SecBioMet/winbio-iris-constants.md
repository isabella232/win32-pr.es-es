---
title: Constantes de WINBIO_IRIS (Winbio \_ Types. h)
description: Especifique los tipos para el reconocimiento de iris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491381"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="dac29-103">WINBIO ( \_ constantes de iris)</span><span class="sxs-lookup"><span data-stu-id="dac29-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="dac29-104">Las siguientes constantes son valores **de \_ \_ subtipo biométrico WINBIO** que se pueden usar para especificar los tipos para el reconocimiento de iris más allá de ANSI INCITS 379-2004: "formato de intercambio de imagen de iris", que no define ningún valor de ojo izquierdo/derecho:</span><span class="sxs-lookup"><span data-stu-id="dac29-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="dac29-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="dac29-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="dac29-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac29-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="dac29-107"><dt> **Tipo de iris de WINBIO \_ \_ \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dac29-108">No se conoce el tipo de iris.</span><span class="sxs-lookup"><span data-stu-id="dac29-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="dac29-109"><dt> **WINBIO \_ de \_ \_ ojo izquierdo de iris**</dt> <dt>0xF5</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="dac29-110">El tipo de iris es el ojo izquierdo.</span><span class="sxs-lookup"><span data-stu-id="dac29-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="dac29-111"><dt> **WINBIO \_ iris \_ derecha \_**</dt> <dt>0xF6</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="dac29-112">El tipo de iris es el ojo adecuado.</span><span class="sxs-lookup"><span data-stu-id="dac29-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="dac29-113"><dt>**WINBIO \_ No se \_ especificó el \_ PDV \_ 01**</dt> <dt>0xF7</dt> de iris</span><span class="sxs-lookup"><span data-stu-id="dac29-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="dac29-114">El subtipo asociado a una primera plantilla de usuario cuando solo hay un ojo es el fotograma de la cámara y no se puede determinar si es el usuario que se encuentra a la izquierda o a la derecha.</span><span class="sxs-lookup"><span data-stu-id="dac29-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="dac29-115"><dt> **WINBIO de \_ iris no especificado de iris \_ \_ \_ 02**</dt> <dt>0xF8</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="dac29-116">Subtipo asociado a una segunda plantilla de usuario cuando solo un ojo es el fotograma de la cámara y no se puede determinar si es el usuario que se encuentra en la parte izquierda o derecha.</span><span class="sxs-lookup"><span data-stu-id="dac29-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="dac29-117"><dt> **WINBIO \_ iris \_ ambos \_ ojos**</dt> <dt>0xF9</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="dac29-118">El tipo de iris es ambos ojos.</span><span class="sxs-lookup"><span data-stu-id="dac29-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="dac29-119"><dt> **WINBIO \_ iris \_ \_**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="dac29-120">El tipo de iris está bien.</span><span class="sxs-lookup"><span data-stu-id="dac29-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="dac29-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac29-121">Requirements</span></span>



| <span data-ttu-id="dac29-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac29-122">Requirement</span></span> | <span data-ttu-id="dac29-123">Value</span><span class="sxs-lookup"><span data-stu-id="dac29-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac29-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac29-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dac29-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac29-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="dac29-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac29-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dac29-127">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac29-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dac29-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dac29-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac29-129"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dac29-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





