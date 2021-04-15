---
title: MCI_OVLY_RECT_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI OVLY \_ Rect \_ parms contiene información de posición de los \_ comandos MCI Put y MCI \_ Where para dispositivos de superposición de vídeo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Estructura de MCI_OVLY_RECT_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488986"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="b55d9-104">MCI \_ OVLY \_ Rect \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="b55d9-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="b55d9-105">La estructura **MCI \_ OVLY \_ Rect \_ parms** contiene información de posición de los comandos [**MCI \_ Put**](mci-put.md) y [**MCI \_ Where**](mci-where.md) para dispositivos de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b55d9-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55d9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b55d9-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="b55d9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b55d9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b55d9-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b55d9-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b55d9-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b55d9-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b55d9-110">**CR**</span><span class="sxs-lookup"><span data-stu-id="b55d9-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="b55d9-111">Rectángulo que contiene información de posición.</span><span class="sxs-lookup"><span data-stu-id="b55d9-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="b55d9-112">Las estructuras [Rect](/previous-versions//ms536136(v=vs.85)) se administran de forma diferente en MCI que en otras partes de Windows. en MCI, **RC. Right** contiene el ancho del rectángulo y **RC. Bottom** contiene el alto.</span><span class="sxs-lookup"><span data-stu-id="b55d9-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b55d9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b55d9-113">Remarks</span></span>

<span data-ttu-id="b55d9-114">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="b55d9-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55d9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b55d9-115">Requirements</span></span>



| <span data-ttu-id="b55d9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b55d9-116">Requirement</span></span> | <span data-ttu-id="b55d9-117">Value</span><span class="sxs-lookup"><span data-stu-id="b55d9-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b55d9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b55d9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b55d9-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b55d9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b55d9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b55d9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b55d9-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b55d9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b55d9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b55d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b55d9-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55d9-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55d9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b55d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55d9-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b55d9-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b55d9-126">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="b55d9-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b55d9-127">**colocación de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b55d9-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="b55d9-128">**MCI \_ donde**</span><span class="sxs-lookup"><span data-stu-id="b55d9-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="b55d9-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b55d9-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b55d9-130">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b55d9-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

