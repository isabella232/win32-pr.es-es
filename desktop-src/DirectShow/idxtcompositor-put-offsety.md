---
description: El \_ método de desplazamiento de put especifica el desplazamiento vertical del rectángulo de destino.
ms.assetid: 68f2774d-9f26-4829-835d-b338c39f1c99
title: 'IDxtCompositor: método de ut_OffsetY de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a20c3812a1fb9756f01ae3a7eb684a6cf6ba0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679051"
---
# <a name="idxtcompositorput_offsety-method"></a><span data-ttu-id="e7195-103">IDxtCompositor::p método de desplazamiento de UT \_</span><span class="sxs-lookup"><span data-stu-id="e7195-103">IDxtCompositor::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="e7195-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e7195-104">\[Deprecated.</span></span> <span data-ttu-id="e7195-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7195-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7195-106">El `put_OffsetY` método especifica el desplazamiento vertical del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="e7195-106">The `put_OffsetY` method specifies the vertical offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7195-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7195-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e7195-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7195-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7195-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7195-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7195-110">Desplazamiento vertical del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e7195-110">The vertical offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7195-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7195-111">Return value</span></span>

<span data-ttu-id="e7195-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e7195-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7195-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7195-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7195-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7195-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7195-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e7195-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7195-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7195-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7195-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e7195-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7195-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7195-118">Requirements</span></span>



| <span data-ttu-id="e7195-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7195-119">Requirement</span></span> | <span data-ttu-id="e7195-120">Value</span><span class="sxs-lookup"><span data-stu-id="e7195-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7195-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7195-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e7195-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7195-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7195-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7195-123">Library</span></span><br/> | <dl> <span data-ttu-id="e7195-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7195-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7195-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7195-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7195-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="e7195-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




