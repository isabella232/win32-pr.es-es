---
description: Sin implementar.
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'IXml2Dex:: WriteXMLPart (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8f194fe409d8ea94f786fe3802b2c758a1a00520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677163"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="d6bb1-103">IXml2Dex:: WriteXMLPart (método)</span><span class="sxs-lookup"><span data-stu-id="d6bb1-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="d6bb1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-104">\[Deprecated.</span></span> <span data-ttu-id="d6bb1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6bb1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d6bb1-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bb1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6bb1-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d6bb1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6bb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bb1-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="d6bb1-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bb1-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d6bb1-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="d6bb1-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bb1-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d6bb1-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="d6bb1-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bb1-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d6bb1-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d6bb1-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d6bb1-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bb1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6bb1-117">Return value</span></span>

<span data-ttu-id="d6bb1-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6bb1-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6bb1-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6bb1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6bb1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6bb1-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6bb1-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6bb1-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d6bb1-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d6bb1-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d6bb1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6bb1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bb1-125">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="d6bb1-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



