---
title: MCI_VD_STEP_PARMS estructura (Mciapi. h)
description: La \_ estructura parms de MCI Vd \_ Step \_ contiene información del comando de paso de MCI \_ para dispositivos de VideoDisc.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- Estructura de MCI_VD_STEP_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534198"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="7081c-104">\_ \_ Paso \_ parms de MCI Vd</span><span class="sxs-lookup"><span data-stu-id="7081c-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="7081c-105">La estructura **parms de MCI \_ Vd \_ Step \_** contiene información del comando de [**\_ paso de MCI**](mci-step.md) para dispositivos de VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="7081c-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7081c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7081c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="7081c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7081c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7081c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="7081c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="7081c-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7081c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="7081c-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="7081c-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="7081c-111">Número de fotogramas que se van a recorrer.</span><span class="sxs-lookup"><span data-stu-id="7081c-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7081c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7081c-112">Remarks</span></span>

<span data-ttu-id="7081c-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="7081c-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="7081c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7081c-114">Requirements</span></span>



| <span data-ttu-id="7081c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7081c-115">Requirement</span></span> | <span data-ttu-id="7081c-116">Value</span><span class="sxs-lookup"><span data-stu-id="7081c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7081c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7081c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7081c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7081c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7081c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7081c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7081c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7081c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7081c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7081c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7081c-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7081c-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7081c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7081c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7081c-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="7081c-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7081c-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="7081c-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="7081c-126">**\_paso MCI**</span><span class="sxs-lookup"><span data-stu-id="7081c-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="7081c-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7081c-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

