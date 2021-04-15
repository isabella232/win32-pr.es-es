---
description: Sin implementar.
ms.assetid: 25300ba5-3578-4eb3-99e2-d547dbb2b9ee
title: IXml2Dex::P método asteXMLFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.PasteXMLFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1e6df8679dde95e7483fe74eb0d8b1b462d51730
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494741"
---
# <a name="ixml2dexpastexmlfile-method"></a><span data-ttu-id="d7b4c-103">IXml2Dex::P método asteXMLFile</span><span class="sxs-lookup"><span data-stu-id="d7b4c-103">IXml2Dex::PasteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="d7b4c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-104">\[Deprecated.</span></span> <span data-ttu-id="d7b4c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7b4c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7b4c-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b4c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7b4c-107">Syntax</span></span>


```C++
HRESULT PasteXMLFile(
   IUnknown *pTimeline,
   double   dStart,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d7b4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7b4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b4c-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="d7b4c-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b4c-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d7b4c-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="d7b4c-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b4c-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d7b4c-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d7b4c-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b4c-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b4c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7b4c-115">Return value</span></span>

<span data-ttu-id="d7b4c-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7b4c-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7b4c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b4c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7b4c-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7b4c-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7b4c-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d7b4c-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d7b4c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7b4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b4c-123">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="d7b4c-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



