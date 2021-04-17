---
description: El \_ método put ReplicateX especifica el número de veces que el patrón de barrido se replica horizontalmente.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: 'IDxtJpeg: método de ut_ReplicateX de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08d892619fe1e6f8222b40d45e634a350e4e9b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679495"
---
# <a name="idxtjpegput_replicatex-method"></a><span data-ttu-id="0c71c-103">IDxtJpeg::p \_ método ReplicateX UT</span><span class="sxs-lookup"><span data-stu-id="0c71c-103">IDxtJpeg::put\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="0c71c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="0c71c-104">\[Deprecated.</span></span> <span data-ttu-id="0c71c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c71c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0c71c-106">El `put_ReplicateX` método especifica el número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="0c71c-106">The `put_ReplicateX` method specifies the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c71c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c71c-107">Syntax</span></span>


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0c71c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c71c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c71c-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c71c-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c71c-110">Número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="0c71c-110">The number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c71c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c71c-111">Return value</span></span>

<span data-ttu-id="0c71c-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0c71c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c71c-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c71c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c71c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c71c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0c71c-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="0c71c-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0c71c-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0c71c-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0c71c-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0c71c-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c71c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c71c-118">Requirements</span></span>



| <span data-ttu-id="0c71c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c71c-119">Requirement</span></span> | <span data-ttu-id="0c71c-120">Value</span><span class="sxs-lookup"><span data-stu-id="0c71c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c71c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c71c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0c71c-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c71c-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0c71c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c71c-123">Library</span></span><br/> | <dl> <span data-ttu-id="0c71c-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c71c-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c71c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c71c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c71c-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="0c71c-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




