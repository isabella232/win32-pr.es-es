---
title: MCI_RECORD_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura parms del registro de MCI contiene información de posicionamiento para el \_ comando MCI record.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- Estructura de MCI_RECORD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488980"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="31b5a-104">\_Estructura parms del registro MCI \_</span><span class="sxs-lookup"><span data-stu-id="31b5a-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="31b5a-105">La **estructura \_ \_ parms del registro de MCI** contiene información de posicionamiento para el comando [**MCI \_ Record**](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="31b5a-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b5a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31b5a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="31b5a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="31b5a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31b5a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="31b5a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="31b5a-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="31b5a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="31b5a-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="31b5a-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="31b5a-111">Posición desde la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="31b5a-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="31b5a-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="31b5a-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="31b5a-113">Posición en la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="31b5a-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31b5a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31b5a-114">Remarks</span></span>

<span data-ttu-id="31b5a-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="31b5a-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b5a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31b5a-116">Requirements</span></span>



| <span data-ttu-id="31b5a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b5a-117">Requirement</span></span> | <span data-ttu-id="31b5a-118">Value</span><span class="sxs-lookup"><span data-stu-id="31b5a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31b5a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31b5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31b5a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="31b5a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="31b5a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31b5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31b5a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31b5a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31b5a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31b5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b5a-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b5a-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b5a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="31b5a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b5a-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="31b5a-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="31b5a-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="31b5a-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="31b5a-128">**registro de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="31b5a-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="31b5a-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31b5a-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

