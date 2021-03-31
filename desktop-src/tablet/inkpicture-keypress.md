---
description: Se produce cuando se presiona una tecla mientras el control InkPicture tiene el foco.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001258"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="e3ce2-103">Evento InkPicture. KeyPress</span><span class="sxs-lookup"><span data-stu-id="e3ce2-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="e3ce2-104">Se produce cuando se presiona una tecla mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="e3ce2-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ce2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3ce2-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="e3ce2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3ce2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ce2-107">*KeyAscii* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3ce2-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ce2-108">Valor ASCII de la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="e3ce2-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ce2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3ce2-109">Return value</span></span>

<span data-ttu-id="e3ce2-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e3ce2-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ce2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3ce2-111">Remarks</span></span>

<span data-ttu-id="e3ce2-112">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="e3ce2-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e3ce2-113">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyPress.</span><span class="sxs-lookup"><span data-stu-id="e3ce2-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ce2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3ce2-114">Requirements</span></span>



| <span data-ttu-id="e3ce2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ce2-115">Requirement</span></span> | <span data-ttu-id="e3ce2-116">Value</span><span class="sxs-lookup"><span data-stu-id="e3ce2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ce2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3ce2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ce2-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e3ce2-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e3ce2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3ce2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ce2-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e3ce2-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e3ce2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3ce2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ce2-122"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e3ce2-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e3ce2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3ce2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3ce2-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3ce2-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e3ce2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3ce2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ce2-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e3ce2-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

