---
title: MCI_WAVE_DELETE_PARMS estructura (Mciapi. h)
description: La \_ estructura parms de MCI Wave \_ Delete \_ contiene información de posición del \_ comando MCI delete para dispositivos de audio de forma de onda.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Estructura de MCI_WAVE_DELETE_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489575"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="b961d-104">\_Estructura parms de MCI Wave \_ Delete \_</span><span class="sxs-lookup"><span data-stu-id="b961d-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="b961d-105">La estructura **parms de MCI \_ Wave \_ Delete \_** contiene información de posición del comando [**MCI \_ Delete**](mci-delete.md) para dispositivos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="b961d-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b961d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b961d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="b961d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b961d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b961d-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b961d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b961d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="b961d-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-111">Posición desde la que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="b961d-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="b961d-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="b961d-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="b961d-113">Posición en la que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="b961d-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b961d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b961d-114">Remarks</span></span>

<span data-ttu-id="b961d-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="b961d-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b961d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b961d-116">Requirements</span></span>



| <span data-ttu-id="b961d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b961d-117">Requirement</span></span> | <span data-ttu-id="b961d-118">Value</span><span class="sxs-lookup"><span data-stu-id="b961d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b961d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b961d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b961d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b961d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b961d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b961d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b961d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b961d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b961d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b961d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b961d-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b961d-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b961d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b961d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b961d-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b961d-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b961d-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="b961d-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b961d-128">**eliminación de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="b961d-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="b961d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b961d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

