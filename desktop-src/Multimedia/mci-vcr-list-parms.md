---
title: MCI_VCR_LIST_PARMS estructura (VCR. h)
description: La estructura parms de la lista de VCR de MCI \_ \_ \_ contiene parámetros para el \_ comando MCI list para los grabadores de casete de vídeo.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- Estructura de MCI_VCR_LIST_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359829"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="5d7ec-104">\_Estructura parms de la lista de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="5d7ec-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="5d7ec-105">La **estructura \_ \_ \_ parms** de la lista de VCR de MCI contiene parámetros para el comando [**MCI \_ List**](mci-list.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5d7ec-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7ec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d7ec-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="5d7ec-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d7ec-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d7ec-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5d7ec-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5d7ec-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="5d7ec-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="5d7ec-111">Búfer para la información devuelta.</span><span class="sxs-lookup"><span data-stu-id="5d7ec-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="5d7ec-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5d7ec-113">Número de entradas de vídeo o audio de VCR.</span><span class="sxs-lookup"><span data-stu-id="5d7ec-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d7ec-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d7ec-114">Remarks</span></span>

<span data-ttu-id="5d7ec-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="5d7ec-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7ec-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7ec-116">Requirements</span></span>



| <span data-ttu-id="5d7ec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7ec-117">Requirement</span></span> | <span data-ttu-id="5d7ec-118">Value</span><span class="sxs-lookup"><span data-stu-id="5d7ec-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d7ec-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7ec-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d7ec-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d7ec-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7ec-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d7ec-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d7ec-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d7ec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7ec-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7ec-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7ec-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d7ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7ec-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5d7ec-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="5d7ec-128">**lista de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="5d7ec-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="5d7ec-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d7ec-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

