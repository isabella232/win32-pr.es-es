---
title: MCI_BREAK_PARMS estructura (Mciapi. h)
description: La \_ estructura de \_ parms de interrupción de MCI contiene código de clave virtual e información de ventana para el comando de interrupción de MCI \_ .
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Estructura de MCI_BREAK_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534017"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="8bb0d-104">\_Estructura parms de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="8bb0d-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="8bb0d-105">La estructura de **\_ \_ parms de interrupción de MCI** contiene código de clave virtual e información de ventana para el comando de [**\_ interrupción de MCI**](mci-break.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb0d-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bb0d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="8bb0d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bb0d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8bb0d-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8bb0d-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8bb0d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8bb0d-110">**nVirtKey**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="8bb0d-111">Código de clave virtual para la clave de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="8bb0d-112">**hwndBreak**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="8bb0d-113">Identificador de la ventana que debe ser la ventana actual para la detección de interrupciones.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bb0d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bb0d-114">Remarks</span></span>

<span data-ttu-id="8bb0d-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="8bb0d-116">Se definen las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8bb0d-116">The following flags are defined:</span></span>

<span data-ttu-id="8bb0d-117">\_hWnd de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="8bb0d-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="8bb0d-118">Valida el miembro **hwndBreak** que especifica la ventana que debe tener el foco para habilitar la detección de interrupciones.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="8bb0d-119">\_tecla de interrupción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="8bb0d-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="8bb0d-120">Valida el miembro de **nVirtKey** que especifica el código de la clave virtual que se va a usar para la clave de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="8bb0d-121">interrupción de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="8bb0d-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="8bb0d-122">Deshabilita cualquier clave de interrupción existente.</span><span class="sxs-lookup"><span data-stu-id="8bb0d-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb0d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb0d-123">Requirements</span></span>



| <span data-ttu-id="8bb0d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb0d-124">Requirement</span></span> | <span data-ttu-id="8bb0d-125">Value</span><span class="sxs-lookup"><span data-stu-id="8bb0d-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb0d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bb0d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb0d-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8bb0d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8bb0d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bb0d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb0d-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8bb0d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8bb0d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bb0d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb0d-131"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb0d-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb0d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb0d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb0d-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8bb0d-134">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8bb0d-135">**interrupción de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="8bb0d-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="8bb0d-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8bb0d-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

