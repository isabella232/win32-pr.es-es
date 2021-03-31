---
title: MCI_VCR_SETTUNER_PARMS estructura (VCR. h)
description: La \_ estructura MCI VCR \_ SETTUNER \_ parms contiene parámetros para el \_ comando MCI SETTUNER para los grabadores de casete de vídeo.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Estructura de MCI_VCR_SETTUNER_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802503"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="d7deb-104">\_SETTUNER MCI \_ VCR \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="d7deb-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="d7deb-105">La estructura **MCI \_ VCR \_ SETTUNER \_ parms** contiene parámetros para el comando [**MCI \_ SETTUNER**](mci-settuner.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d7deb-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7deb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7deb-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="d7deb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7deb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7deb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d7deb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d7deb-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d7deb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d7deb-110">**dwChannel**</span><span class="sxs-lookup"><span data-stu-id="d7deb-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="d7deb-111">Nuevo número de canal.</span><span class="sxs-lookup"><span data-stu-id="d7deb-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="d7deb-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="d7deb-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d7deb-113">Sintonizador lógico al que afecta el comando [**\_ SETTUNER de MCI**](mci-settuner.md) .</span><span class="sxs-lookup"><span data-stu-id="d7deb-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7deb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7deb-114">Remarks</span></span>

<span data-ttu-id="d7deb-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="d7deb-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7deb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7deb-116">Requirements</span></span>



| <span data-ttu-id="d7deb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7deb-117">Requirement</span></span> | <span data-ttu-id="d7deb-118">Value</span><span class="sxs-lookup"><span data-stu-id="d7deb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7deb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7deb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d7deb-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7deb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7deb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7deb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d7deb-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7deb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7deb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7deb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7deb-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7deb-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7deb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7deb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7deb-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d7deb-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d7deb-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="d7deb-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d7deb-128">**MCI \_ SETTUNER**</span><span class="sxs-lookup"><span data-stu-id="d7deb-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="d7deb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7deb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

