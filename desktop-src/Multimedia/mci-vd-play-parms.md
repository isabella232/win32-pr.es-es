---
title: MCI_VD_PLAY_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI Vd \_ Play \_ parms contiene información sobre la posición y la velocidad del comando MCI \_ Play para dispositivos de VideoDisc.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Estructura de MCI_VD_PLAY_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079414"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="5bc0a-104">MCI \_ Vd \_ Play \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="5bc0a-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="5bc0a-105">La estructura **MCI \_ Vd \_ Play \_ parms** contiene información sobre la posición y la velocidad del comando [**MCI \_ Play**](mci-play.md) para dispositivos de VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc0a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bc0a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="5bc0a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5bc0a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5bc0a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5bc0a-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5bc0a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="5bc0a-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="5bc0a-111">Posición desde la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="5bc0a-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="5bc0a-113">Posición en la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="5bc0a-114">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="5bc0a-115">Velocidad de reproducción en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc0a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bc0a-116">Remarks</span></span>

<span data-ttu-id="5bc0a-117">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="5bc0a-118">Puede usar la estructura [**de \_ \_ parms de reproducción de MCI**](mci-play-parms.md) en lugar de **MCI \_ Vd \_ Play \_ parms** si no está usando los miembros de datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-119">Requirements</span></span>



| <span data-ttu-id="5bc0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc0a-120">Requirement</span></span> | <span data-ttu-id="5bc0a-121">Value</span><span class="sxs-lookup"><span data-stu-id="5bc0a-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc0a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc0a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc0a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bc0a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5bc0a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc0a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc0a-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bc0a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5bc0a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bc0a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bc0a-127"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc0a-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc0a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bc0a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc0a-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5bc0a-130">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="5bc0a-131">**reproducción de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="5bc0a-132">**\_parms de reproducción de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="5bc0a-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5bc0a-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

