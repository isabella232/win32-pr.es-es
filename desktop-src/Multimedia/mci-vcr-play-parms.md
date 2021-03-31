---
title: MCI_VCR_PLAY_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ Play \_ parms contiene parámetros para el comando de reproducción de MCI para los \_ grabadores de casete de vídeo.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Estructura de MCI_VCR_PLAY_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996500"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="c7975-104">\_Parms MCI VCR \_ Play \_ Structure</span><span class="sxs-lookup"><span data-stu-id="c7975-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="c7975-105">La estructura **MCI \_ VCR \_ Play \_ parms** contiene parámetros para el comando de [**\_ reproducción de MCI**](mci-play.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c7975-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7975-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7975-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="c7975-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7975-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7975-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c7975-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c7975-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c7975-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c7975-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="c7975-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="c7975-111">Posición desde la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="c7975-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="c7975-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c7975-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c7975-113">Posición en la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="c7975-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="c7975-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="c7975-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="c7975-115">Valor de tiempo que afecta al comando [**MCI \_ Play**](mci-play.md) o [**MCI \_ CUE**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="c7975-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="c7975-116">En el caso de [**MCI \_ Play**](mci-play-parms.md), es el momento en que comienza la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c7975-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="c7975-117">En el caso de **MCI \_**, es el momento en que el dispositivo señalado alcanza la posición proporcionada en **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="c7975-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7975-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7975-118">Remarks</span></span>

<span data-ttu-id="c7975-119">Las posiciones se especifican en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="c7975-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="c7975-120">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="c7975-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7975-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7975-121">Requirements</span></span>



| <span data-ttu-id="c7975-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7975-122">Requirement</span></span> | <span data-ttu-id="c7975-123">Value</span><span class="sxs-lookup"><span data-stu-id="c7975-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7975-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7975-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c7975-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7975-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c7975-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7975-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c7975-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7975-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c7975-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7975-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7975-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7975-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7975-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7975-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7975-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c7975-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c7975-132">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="c7975-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c7975-133">**\_pista MCI**</span><span class="sxs-lookup"><span data-stu-id="c7975-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="c7975-134">**reproducción de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="c7975-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="c7975-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7975-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

