---
description: El \_ método get scaleX recupera la cantidad por la que se ajusta horizontalmente el borrado.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Método IDxtJpeg:: get_ScaleX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680191"
---
# <a name="idxtjpegget_scalex-method"></a><span data-ttu-id="1668b-103">IDxtJpeg:: get \_ scaleX (método)</span><span class="sxs-lookup"><span data-stu-id="1668b-103">IDxtJpeg::get\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="1668b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1668b-104">\[Deprecated.</span></span> <span data-ttu-id="1668b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1668b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1668b-106">El `get_ScaleX` método recupera la cantidad por la que se ajusta horizontalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="1668b-106">The `get_ScaleX` method retrieves the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="1668b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1668b-107">Syntax</span></span>


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1668b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1668b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1668b-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1668b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1668b-110">Recibe la cantidad por la que se ajusta horizontalmente el borrado, como un porcentaje de la definición de borrado original.</span><span class="sxs-lookup"><span data-stu-id="1668b-110">Receives the amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="1668b-111">Por ejemplo, el valor 1,0 significa que no hay expansión y 2,0 significa que el 200% se ajusta.</span><span class="sxs-lookup"><span data-stu-id="1668b-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1668b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1668b-112">Return value</span></span>

<span data-ttu-id="1668b-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1668b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1668b-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1668b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1668b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1668b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1668b-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1668b-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1668b-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1668b-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1668b-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1668b-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1668b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1668b-119">Requirements</span></span>



| <span data-ttu-id="1668b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1668b-120">Requirement</span></span> | <span data-ttu-id="1668b-121">Value</span><span class="sxs-lookup"><span data-stu-id="1668b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1668b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1668b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1668b-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1668b-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1668b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1668b-124">Library</span></span><br/> | <dl> <span data-ttu-id="1668b-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1668b-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1668b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1668b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1668b-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="1668b-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




