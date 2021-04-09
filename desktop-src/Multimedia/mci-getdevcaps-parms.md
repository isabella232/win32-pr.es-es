---
title: MCI_GETDEVCAPS_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI GETDEVCAPS \_ parms contiene información sobre la capacidad del dispositivo para el \_ comando MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Estructura de MCI_GETDEVCAPS_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079065"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="6687e-104">\_GETDEVCAPS MCI \_ parms estructura</span><span class="sxs-lookup"><span data-stu-id="6687e-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="6687e-105">La estructura **MCI \_ GETDEVCAPS \_ parms** contiene información sobre la capacidad del dispositivo para el comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="6687e-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6687e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6687e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="6687e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6687e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6687e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6687e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6687e-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6687e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6687e-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="6687e-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="6687e-111">Contiene información sobre la salida.</span><span class="sxs-lookup"><span data-stu-id="6687e-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="6687e-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="6687e-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="6687e-113">Capacidad que se consulta.</span><span class="sxs-lookup"><span data-stu-id="6687e-113">Capability being queried.</span></span> <span data-ttu-id="6687e-114">Este miembro puede ser una de las constantes enumeradas en el material de referencia del comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="6687e-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6687e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6687e-115">Remarks</span></span>

<span data-ttu-id="6687e-116">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="6687e-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6687e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6687e-117">Requirements</span></span>



| <span data-ttu-id="6687e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6687e-118">Requirement</span></span> | <span data-ttu-id="6687e-119">Value</span><span class="sxs-lookup"><span data-stu-id="6687e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6687e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6687e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6687e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6687e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6687e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6687e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6687e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6687e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6687e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6687e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6687e-125"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6687e-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6687e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6687e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6687e-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6687e-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6687e-128">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="6687e-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6687e-129">**MCI \_ GETDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="6687e-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="6687e-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6687e-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

