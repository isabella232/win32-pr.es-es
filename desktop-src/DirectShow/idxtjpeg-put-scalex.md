---
description: El \_ método put scaleX especifica la cantidad por la que se ajusta horizontalmente el borrado.
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: 'IDxtJpeg: método de ut_ScaleX de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fff0583ce3163ebf5626cfdbb82edf5c927bdc9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679328"
---
# <a name="idxtjpegput_scalex-method"></a><span data-ttu-id="a1ccb-103">IDxtJpeg::p UT ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="a1ccb-103">IDxtJpeg::put\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="a1ccb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-104">\[Deprecated.</span></span> <span data-ttu-id="a1ccb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1ccb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1ccb-106">El `put_ScaleX` método especifica la cantidad por la que se ajusta horizontalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-106">The `put_ScaleX` method specifies the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ccb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1ccb-107">Syntax</span></span>


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a1ccb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1ccb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1ccb-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1ccb-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1ccb-110">Cantidad en la que se ajusta horizontalmente el borrado, como porcentaje de la definición de borrador original.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-110">The amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="a1ccb-111">Por ejemplo, el valor 1,0 significa que no hay expansión y 2,0 significa que el 200% se ajusta.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1ccb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1ccb-112">Return value</span></span>

<span data-ttu-id="a1ccb-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1ccb-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1ccb-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ccb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1ccb-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1ccb-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1ccb-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1ccb-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1ccb-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1ccb-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1ccb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1ccb-119">Requirements</span></span>



| <span data-ttu-id="a1ccb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1ccb-120">Requirement</span></span> | <span data-ttu-id="a1ccb-121">Value</span><span class="sxs-lookup"><span data-stu-id="a1ccb-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ccb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1ccb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a1ccb-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ccb-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1ccb-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1ccb-124">Library</span></span><br/> | <dl> <span data-ttu-id="a1ccb-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1ccb-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1ccb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1ccb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1ccb-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="a1ccb-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




