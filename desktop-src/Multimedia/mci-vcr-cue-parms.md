---
title: MCI_VCR_CUE_PARMS estructura (VCR. h)
description: La \_ estructura de parms VCR de MCI \_ \_ contiene parámetros para el \_ comando MCI CUE para los grabadores de casete de vídeo.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- Estructura de MCI_VCR_CUE_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905572"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="c2170-104">\_ \_ Estructura parms de vídeo de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c2170-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="c2170-105">La estructura de **\_ \_ \_ parms VCR de MCI** contiene parámetros para el comando [**MCI \_ CUE**](mci-cue.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2170-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2170-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2170-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="c2170-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2170-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2170-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c2170-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c2170-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c2170-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c2170-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="c2170-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="c2170-111">Posición desde la que se va a señalar.</span><span class="sxs-lookup"><span data-stu-id="c2170-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="c2170-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c2170-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c2170-113">Posición en la que se va a señalar.</span><span class="sxs-lookup"><span data-stu-id="c2170-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2170-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2170-114">Remarks</span></span>

<span data-ttu-id="c2170-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="c2170-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2170-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2170-116">Requirements</span></span>



| <span data-ttu-id="c2170-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2170-117">Requirement</span></span> | <span data-ttu-id="c2170-118">Value</span><span class="sxs-lookup"><span data-stu-id="c2170-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c2170-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2170-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2170-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c2170-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c2170-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2170-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2170-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2170-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2170-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2170-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2170-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2170-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2170-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2170-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2170-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c2170-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c2170-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="c2170-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c2170-128">**\_pista MCI**</span><span class="sxs-lookup"><span data-stu-id="c2170-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="c2170-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2170-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

