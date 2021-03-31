---
title: MCI_VCR_SETAUDIO_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ SETAUDIO \_ parms contiene parámetros para el \_ comando MCI SETAUDIO para los grabadores de casete de vídeo.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- Estructura de MCI_VCR_SETAUDIO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905058"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="10839-104">\_SETAUDIO MCI \_ VCR \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="10839-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="10839-105">La estructura **MCI \_ VCR \_ SETAUDIO \_ parms** contiene parámetros para el comando [**MCI \_ SETAUDIO**](mci-setaudio.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10839-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="10839-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10839-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="10839-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="10839-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="10839-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="10839-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="10839-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="10839-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="10839-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="10839-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="10839-111">Pista de audio.</span><span class="sxs-lookup"><span data-stu-id="10839-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="10839-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="10839-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="10839-113">Tipo de entrada o entrada supervisada.</span><span class="sxs-lookup"><span data-stu-id="10839-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="10839-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="10839-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="10839-115">Entrada de audio (del tipo especificado en el miembro **dwTo** ) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="10839-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10839-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10839-116">Remarks</span></span>

<span data-ttu-id="10839-117">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="10839-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="10839-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10839-118">Requirements</span></span>



| <span data-ttu-id="10839-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10839-119">Requirement</span></span> | <span data-ttu-id="10839-120">Value</span><span class="sxs-lookup"><span data-stu-id="10839-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="10839-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10839-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10839-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="10839-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="10839-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10839-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10839-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10839-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="10839-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10839-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10839-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="10839-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10839-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="10839-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10839-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="10839-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="10839-129">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="10839-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="10839-130">**MCI \_ SETAUDIO**</span><span class="sxs-lookup"><span data-stu-id="10839-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="10839-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10839-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

