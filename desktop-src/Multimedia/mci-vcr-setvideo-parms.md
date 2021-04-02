---
title: MCI_VCR_SETVIDEO_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ SETVIDEO \_ parms contiene parámetros para el \_ comando MCI SETVIDEO para los grabadores de casete de vídeo.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Estructura de MCI_VCR_SETVIDEO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905538"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="c93e8-104">\_SETVIDEO MCI \_ VCR \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="c93e8-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="c93e8-105">La estructura **MCI \_ VCR \_ SETVIDEO \_ parms** contiene parámetros para el comando [**MCI \_ SETVIDEO**](mci-setvideo.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c93e8-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93e8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c93e8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="c93e8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c93e8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c93e8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c93e8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c93e8-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c93e8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c93e8-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="c93e8-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="c93e8-111">Pista afectada.</span><span class="sxs-lookup"><span data-stu-id="c93e8-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="c93e8-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c93e8-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c93e8-113">Tipo de entrada o entrada supervisada.</span><span class="sxs-lookup"><span data-stu-id="c93e8-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="c93e8-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="c93e8-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c93e8-115">Entrada de vídeo (del tipo especificado en el miembro **dwTo** ) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c93e8-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c93e8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c93e8-116">Remarks</span></span>

<span data-ttu-id="c93e8-117">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="c93e8-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93e8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c93e8-118">Requirements</span></span>



| <span data-ttu-id="c93e8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c93e8-119">Requirement</span></span> | <span data-ttu-id="c93e8-120">Value</span><span class="sxs-lookup"><span data-stu-id="c93e8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c93e8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c93e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c93e8-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c93e8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c93e8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c93e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c93e8-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c93e8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c93e8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c93e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c93e8-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93e8-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93e8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c93e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93e8-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c93e8-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c93e8-129">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="c93e8-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c93e8-130">**MCI \_ SETVIDEO**</span><span class="sxs-lookup"><span data-stu-id="c93e8-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="c93e8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c93e8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

