---
description: El \_ método get ReplicateX recupera el número de veces que el patrón de barrido se replica horizontalmente.
ms.assetid: 669a3bde-af8b-4d31-b914-41b71c95de1c
title: 'Método IDxtJpeg:: get_ReplicateX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8855f819cb00d46297220c41deb6b81d6150e0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680671"
---
# <a name="idxtjpegget_replicatex-method"></a><span data-ttu-id="81d31-103">IDxtJpeg:: get \_ ReplicateX (método)</span><span class="sxs-lookup"><span data-stu-id="81d31-103">IDxtJpeg::get\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="81d31-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="81d31-104">\[Deprecated.</span></span> <span data-ttu-id="81d31-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81d31-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81d31-106">El `get_ReplicateX` método recupera el número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="81d31-106">The `get_ReplicateX` method retrieves the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81d31-107">Syntax</span></span>


```C++
HRESULT get_ReplicateX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="81d31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81d31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d31-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="81d31-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81d31-110">Recibe el número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="81d31-110">Receives the number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d31-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81d31-111">Return value</span></span>

<span data-ttu-id="81d31-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="81d31-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81d31-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81d31-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d31-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81d31-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81d31-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="81d31-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81d31-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81d31-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81d31-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81d31-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81d31-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d31-118">Requirements</span></span>



| <span data-ttu-id="81d31-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d31-119">Requirement</span></span> | <span data-ttu-id="81d31-120">Value</span><span class="sxs-lookup"><span data-stu-id="81d31-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81d31-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81d31-121">Header</span></span><br/>  | <dl> <span data-ttu-id="81d31-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d31-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81d31-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81d31-123">Library</span></span><br/> | <dl> <span data-ttu-id="81d31-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81d31-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d31-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="81d31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d31-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="81d31-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




