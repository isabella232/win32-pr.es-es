---
description: El \_ método put Replication especifica el número de veces que el patrón de barrido se replica verticalmente.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: 'IDxtJpeg: método de ut_ReplicateY de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ac5016635cb8e6f5b81b99f1ea67f0282878d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680232"
---
# <a name="idxtjpegput_replicatey-method"></a><span data-ttu-id="16d15-103">IDxtJpeg::p \_ método de replicación UT</span><span class="sxs-lookup"><span data-stu-id="16d15-103">IDxtJpeg::put\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="16d15-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="16d15-104">\[Deprecated.</span></span> <span data-ttu-id="16d15-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16d15-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16d15-106">El `put_ReplicateY` método especifica el número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="16d15-106">The `put_ReplicateY` method specifies the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d15-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16d15-107">Syntax</span></span>


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="16d15-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16d15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16d15-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16d15-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16d15-110">Número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="16d15-110">The number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16d15-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16d15-111">Return value</span></span>

<span data-ttu-id="16d15-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="16d15-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16d15-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16d15-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16d15-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16d15-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16d15-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="16d15-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16d15-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16d15-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16d15-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16d15-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16d15-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16d15-118">Requirements</span></span>



| <span data-ttu-id="16d15-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16d15-119">Requirement</span></span> | <span data-ttu-id="16d15-120">Value</span><span class="sxs-lookup"><span data-stu-id="16d15-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16d15-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16d15-121">Header</span></span><br/>  | <dl> <span data-ttu-id="16d15-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="16d15-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16d15-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16d15-123">Library</span></span><br/> | <dl> <span data-ttu-id="16d15-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16d15-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d15-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="16d15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d15-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="16d15-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




