---
title: MCI_VCR_STEP_PARMS estructura (VCR. h)
description: La \_ estructura parms VCR de MCI \_ \_ contiene los parámetros del comando de paso de MCI \_ para los grabadores de casete de vídeo.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- Estructura de MCI_VCR_STEP_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078983"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="60b1b-104">\_ \_ Estructura parms del VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="60b1b-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="60b1b-105">La **estructura \_ \_ \_ parms VCR de MCI** contiene los parámetros del comando de [**\_ paso de MCI**](mci-step.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="60b1b-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b1b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60b1b-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="60b1b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="60b1b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="60b1b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="60b1b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="60b1b-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="60b1b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="60b1b-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="60b1b-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="60b1b-111">Número de fotogramas que se van a saltar (la longitud de un solo paso), ya que el comando de [**\_ paso de MCI**](mci-step.md) avanza o retrocede por el contenido.</span><span class="sxs-lookup"><span data-stu-id="60b1b-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b1b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60b1b-112">Remarks</span></span>

<span data-ttu-id="60b1b-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="60b1b-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b1b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b1b-114">Requirements</span></span>



| <span data-ttu-id="60b1b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b1b-115">Requirement</span></span> | <span data-ttu-id="60b1b-116">Value</span><span class="sxs-lookup"><span data-stu-id="60b1b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="60b1b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60b1b-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="60b1b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="60b1b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="60b1b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60b1b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="60b1b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60b1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b1b-122"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b1b-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b1b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b1b-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="60b1b-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="60b1b-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="60b1b-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="60b1b-126">**\_paso MCI**</span><span class="sxs-lookup"><span data-stu-id="60b1b-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="60b1b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60b1b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

