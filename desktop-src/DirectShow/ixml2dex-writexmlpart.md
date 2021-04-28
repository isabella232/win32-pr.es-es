---
description: 'Método IXml2Dex::WriteXMLPart: no implementado.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: IXml2Dex::WriteXMLPart (método)
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
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084381"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="0e32d-103">IXml2Dex::WriteXMLPart (método)</span><span class="sxs-lookup"><span data-stu-id="0e32d-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="0e32d-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0e32d-104">\[Deprecated.</span></span> <span data-ttu-id="0e32d-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e32d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e32d-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="0e32d-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e32d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e32d-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="0e32d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e32d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e32d-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="0e32d-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="0e32d-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0e32d-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e32d-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="0e32d-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0e32d-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0e32d-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e32d-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="0e32d-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0e32d-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0e32d-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0e32d-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="0e32d-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="0e32d-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0e32d-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e32d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e32d-117">Return value</span></span>

<span data-ttu-id="0e32d-118">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0e32d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e32d-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0e32d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e32d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e32d-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e32d-121">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="0e32d-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e32d-122">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e32d-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e32d-123">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0e32d-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0e32d-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0e32d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e32d-125">**IXml2Dex (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="0e32d-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



