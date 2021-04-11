---
title: Constantes de WINBIO_ANSI_385_FACE (Winbio \_ Types. h)
description: Especifique los tipos de imagen frontal facial para el reconocimiento facial.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150863"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="ea2e2-103">WINBIO \_ \_ constantes de \_ tipo ANSI 385</span><span class="sxs-lookup"><span data-stu-id="ea2e2-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="ea2e2-104">Las siguientes constantes son valores **de \_ \_ subtipo biométrico WINBIO** que se pueden usar para especificar los dos tipos de imágenes de la esfera frontal según se define en ANSI INCITS 385-2004: "formato de reconocimiento facial para el intercambio de datos": resolución completa y baja resolución.</span><span class="sxs-lookup"><span data-stu-id="ea2e2-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="ea2e2-105">En la práctica, el marco biométrico solo usará imágenes de resolución completa para el reconocimiento facial.</span><span class="sxs-lookup"><span data-stu-id="ea2e2-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="ea2e2-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="ea2e2-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="ea2e2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea2e2-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="ea2e2-108"><dt>**WINBIO \_ \_Tipo de \_ letra ANSI 385 \_ \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea2e2-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="ea2e2-109">Se desconoce el tipo de imagen de la esfera frontal.</span><span class="sxs-lookup"><span data-stu-id="ea2e2-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="ea2e2-110"><dt>**WINBIO \_ ANSI \_ 385 con una \_ superficie \_ \_ completa**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ea2e2-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="ea2e2-111">El tipo de imagen de la esfera frontal es resolución completa.</span><span class="sxs-lookup"><span data-stu-id="ea2e2-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="ea2e2-112"><dt>**WINBIO \_ \_ \_ \_ \_ Token**</dt> <dt>2</dt> de la superficie ANSI 385</span><span class="sxs-lookup"><span data-stu-id="ea2e2-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="ea2e2-113">El tipo de imagen de la esfera frontal es baja resolución.</span><span class="sxs-lookup"><span data-stu-id="ea2e2-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="ea2e2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea2e2-114">Requirements</span></span>



| <span data-ttu-id="ea2e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea2e2-115">Requirement</span></span> | <span data-ttu-id="ea2e2-116">Value</span><span class="sxs-lookup"><span data-stu-id="ea2e2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2e2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea2e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ea2e2-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea2e2-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ea2e2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea2e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ea2e2-120">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea2e2-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ea2e2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea2e2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea2e2-122"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea2e2-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





