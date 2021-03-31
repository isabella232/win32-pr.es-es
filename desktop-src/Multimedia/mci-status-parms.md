---
title: MCI_STATUS_PARMS estructura (Mciapi. h)
description: La \_ estructura de \_ parms de estado de MCI contiene información para el \_ comando MCI status.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Estructura de MCI_STATUS_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996047"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="77bfc-104">\_Estructura parms de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="77bfc-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="77bfc-105">La estructura de **\_ \_ parms de estado de MCI** contiene información para el comando [**MCI \_ status**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="77bfc-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bfc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77bfc-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="77bfc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="77bfc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="77bfc-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="77bfc-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="77bfc-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="77bfc-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="77bfc-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="77bfc-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="77bfc-111">Contiene información sobre la devolución.</span><span class="sxs-lookup"><span data-stu-id="77bfc-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="77bfc-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="77bfc-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="77bfc-113">Capacidad que se consulta.</span><span class="sxs-lookup"><span data-stu-id="77bfc-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="77bfc-114">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="77bfc-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="77bfc-115">Longitud o número de pistas.</span><span class="sxs-lookup"><span data-stu-id="77bfc-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77bfc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77bfc-116">Remarks</span></span>

<span data-ttu-id="77bfc-117">La \_ marca del \_ elemento de estado de MCI debe establecerse en el parámetro *fdwCommand* de la función [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar el miembro **dwItem** , que debe contener una de las constantes que indican qué información de estado se solicita.</span><span class="sxs-lookup"><span data-stu-id="77bfc-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bfc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77bfc-118">Requirements</span></span>



| <span data-ttu-id="77bfc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77bfc-119">Requirement</span></span> | <span data-ttu-id="77bfc-120">Value</span><span class="sxs-lookup"><span data-stu-id="77bfc-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77bfc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77bfc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77bfc-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="77bfc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="77bfc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77bfc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77bfc-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77bfc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="77bfc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77bfc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77bfc-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77bfc-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77bfc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="77bfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bfc-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="77bfc-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="77bfc-129">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="77bfc-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="77bfc-130">**Estado de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="77bfc-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="77bfc-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77bfc-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

