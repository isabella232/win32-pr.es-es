---
description: Se produce después de cambiarse la propiedad SizeMode del control InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture. SizeModeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361330"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="663f8-103">Evento InkPicture. SizeModeChanged</span><span class="sxs-lookup"><span data-stu-id="663f8-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="663f8-104">Se produce después de cambiarse la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="663f8-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="663f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="663f8-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="663f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="663f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="663f8-107">*Newmode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="663f8-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="663f8-108">Nuevo estado del control [InkPicture](inkpicture-control-reference.md) , basado en el nuevo valor de la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="663f8-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="663f8-109">*OldMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="663f8-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="663f8-110">Estado anterior del control [InkPicture](inkpicture-control-reference.md) , basado en el valor anterior de la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="663f8-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="663f8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="663f8-111">Return value</span></span>

<span data-ttu-id="663f8-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="663f8-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="663f8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="663f8-113">Remarks</span></span>

<span data-ttu-id="663f8-114">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="663f8-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="663f8-115">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPESizeModeChanged.</span><span class="sxs-lookup"><span data-stu-id="663f8-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="663f8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="663f8-116">Requirements</span></span>



| <span data-ttu-id="663f8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="663f8-117">Requirement</span></span> | <span data-ttu-id="663f8-118">Value</span><span class="sxs-lookup"><span data-stu-id="663f8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="663f8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="663f8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="663f8-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="663f8-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="663f8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="663f8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="663f8-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="663f8-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="663f8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="663f8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="663f8-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="663f8-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="663f8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="663f8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="663f8-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="663f8-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="663f8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="663f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="663f8-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="663f8-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

