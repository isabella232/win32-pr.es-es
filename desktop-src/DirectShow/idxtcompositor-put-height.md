---
description: El \_ método put height especifica el alto del rectángulo de destino.
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: 'IDxtCompositor: método de ut_Height de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680192"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="7b903-103">IDxtCompositor: método de alto de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="7b903-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="7b903-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7b903-104">\[Deprecated.</span></span> <span data-ttu-id="7b903-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b903-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b903-106">El `put_Height` método especifica el alto del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="7b903-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b903-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b903-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7b903-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b903-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b903-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b903-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b903-110">Alto del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7b903-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b903-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b903-111">Return value</span></span>

<span data-ttu-id="7b903-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7b903-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b903-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b903-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b903-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b903-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b903-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7b903-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b903-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b903-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7b903-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7b903-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b903-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b903-118">Requirements</span></span>



| <span data-ttu-id="7b903-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b903-119">Requirement</span></span> | <span data-ttu-id="7b903-120">Value</span><span class="sxs-lookup"><span data-stu-id="7b903-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b903-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b903-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7b903-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b903-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7b903-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b903-123">Library</span></span><br/> | <dl> <span data-ttu-id="7b903-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b903-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b903-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b903-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b903-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="7b903-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




