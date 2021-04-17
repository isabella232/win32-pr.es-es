---
title: MCI_VCR_RECORD_PARMS estructura (VCR. h)
description: La \_ estructura parms del registro VCR de MCI \_ \_ contiene los parámetros para el \_ comando MCI record para los grabadores de casete de vídeo.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Estructura de MCI_VCR_RECORD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676702"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="79174-104">\_ \_ Estructura parms del registro VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="79174-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="79174-105">La **estructura \_ \_ \_ parms del registro VCR de MCI** contiene los parámetros para el comando [**MCI \_ Record**](mci-record.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79174-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="79174-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79174-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="79174-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="79174-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="79174-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="79174-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="79174-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="79174-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="79174-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="79174-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="79174-111">Posición desde la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="79174-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="79174-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="79174-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="79174-113">Posición en la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="79174-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="79174-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="79174-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="79174-115">Valor de tiempo que afecta al comando [**MCI \_ Record**](mci-record.md) o [**MCI \_ CUE**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="79174-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="79174-116">En el caso del **\_ registro MCI**, es el momento en el que comienza la grabación.</span><span class="sxs-lookup"><span data-stu-id="79174-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="79174-117">En el caso de **MCI \_**, es el momento en que el dispositivo señalado alcanza la posición proporcionada en **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="79174-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79174-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79174-118">Remarks</span></span>

<span data-ttu-id="79174-119">Las posiciones se especifican en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="79174-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="79174-120">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="79174-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="79174-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79174-121">Requirements</span></span>



| <span data-ttu-id="79174-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79174-122">Requirement</span></span> | <span data-ttu-id="79174-123">Value</span><span class="sxs-lookup"><span data-stu-id="79174-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="79174-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79174-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79174-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="79174-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79174-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79174-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79174-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79174-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79174-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79174-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79174-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="79174-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79174-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="79174-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79174-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="79174-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="79174-132">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="79174-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="79174-133">**\_pista MCI**</span><span class="sxs-lookup"><span data-stu-id="79174-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="79174-134">**registro de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="79174-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="79174-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79174-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

