---
description: El \_ método get replicate recupera el número de veces que el patrón de barrido se replica verticalmente.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'Método IDxtJpeg:: get_ReplicateY (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681156"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="22bf2-103">IDxtJpeg:: get \_ replicate (método)</span><span class="sxs-lookup"><span data-stu-id="22bf2-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="22bf2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="22bf2-104">\[Deprecated.</span></span> <span data-ttu-id="22bf2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22bf2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22bf2-106">El `get_ReplicateY` método recupera el número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="22bf2-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="22bf2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22bf2-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="22bf2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22bf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22bf2-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="22bf2-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="22bf2-110">Recibe el número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="22bf2-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22bf2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22bf2-111">Return value</span></span>

<span data-ttu-id="22bf2-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="22bf2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22bf2-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22bf2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22bf2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22bf2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22bf2-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="22bf2-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22bf2-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22bf2-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22bf2-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="22bf2-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22bf2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22bf2-118">Requirements</span></span>



| <span data-ttu-id="22bf2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22bf2-119">Requirement</span></span> | <span data-ttu-id="22bf2-120">Value</span><span class="sxs-lookup"><span data-stu-id="22bf2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22bf2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22bf2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22bf2-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="22bf2-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22bf2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22bf2-123">Library</span></span><br/> | <dl> <span data-ttu-id="22bf2-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22bf2-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22bf2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="22bf2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22bf2-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="22bf2-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




