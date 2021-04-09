---
title: MCI_SET_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura de parms de MCI set contiene información para el \_ comando MCI set.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- Estructura de MCI_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079060"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="4e9ef-104">\_ \_ Estructura parms de MCI set</span><span class="sxs-lookup"><span data-stu-id="4e9ef-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="4e9ef-105">La estructura de **\_ \_ parms de MCI Set** contiene información para el comando [**MCI \_ set**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4e9ef-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e9ef-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e9ef-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="4e9ef-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e9ef-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e9ef-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4e9ef-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="4e9ef-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4e9ef-111">Formato de hora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="4e9ef-113">Canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e9ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e9ef-114">Remarks</span></span>

<span data-ttu-id="4e9ef-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9ef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e9ef-116">Requirements</span></span>



| <span data-ttu-id="4e9ef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e9ef-117">Requirement</span></span> | <span data-ttu-id="4e9ef-118">Value</span><span class="sxs-lookup"><span data-stu-id="4e9ef-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9ef-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e9ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e9ef-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4e9ef-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4e9ef-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e9ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e9ef-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e9ef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4e9ef-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e9ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e9ef-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e9ef-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9ef-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e9ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9ef-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4e9ef-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="4e9ef-128">**MCI \_ set**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="4e9ef-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e9ef-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

