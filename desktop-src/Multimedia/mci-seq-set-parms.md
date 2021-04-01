---
title: MCI_SEQ_SET_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI SEQ \_ set \_ parms contiene información para el comando MCI \_ set para dispositivos MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Estructura de MCI_SEQ_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996048"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="8065c-104">MCI \_ Seq \_ set \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="8065c-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="8065c-105">La estructura **MCI \_ Seq \_ set \_ parms** contiene información para el comando [**MCI \_ set**](mci-set.md) para dispositivos MIDI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="8065c-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8065c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8065c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="8065c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8065c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8065c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8065c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8065c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="8065c-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-111">Formato de hora del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="8065c-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="8065c-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-113">Canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="8065c-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-114">**dwTempo**</span><span class="sxs-lookup"><span data-stu-id="8065c-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-115">Ritmo.</span><span class="sxs-lookup"><span data-stu-id="8065c-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-116">**dwPort**</span><span class="sxs-lookup"><span data-stu-id="8065c-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-117">Puerto</span><span class="sxs-lookup"><span data-stu-id="8065c-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-118">**dwSlave**</span><span class="sxs-lookup"><span data-stu-id="8065c-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-119">Tipo de sincronización utilizada por el secuenciador para la operación subordinada.</span><span class="sxs-lookup"><span data-stu-id="8065c-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-120">**dwMaster**</span><span class="sxs-lookup"><span data-stu-id="8065c-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-121">Tipo de sincronización utilizada por el secuenciador para la operación maestra.</span><span class="sxs-lookup"><span data-stu-id="8065c-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="8065c-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="8065c-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8065c-123">Desplazamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="8065c-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8065c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8065c-124">Remarks</span></span>

<span data-ttu-id="8065c-125">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="8065c-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8065c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8065c-126">Requirements</span></span>



| <span data-ttu-id="8065c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8065c-127">Requirement</span></span> | <span data-ttu-id="8065c-128">Value</span><span class="sxs-lookup"><span data-stu-id="8065c-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8065c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8065c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8065c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8065c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8065c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8065c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8065c-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8065c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8065c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8065c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8065c-134"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8065c-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8065c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8065c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8065c-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8065c-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8065c-137">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="8065c-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8065c-138">**MCI \_ set**</span><span class="sxs-lookup"><span data-stu-id="8065c-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="8065c-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8065c-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

