---
description: 'Método IXml2Dex::CreateGraphFromFile: no implementado.'
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: IXml2Dex::CreateGraphFromFile (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: a79b4115dddb0e15adb4284bbefd245aba088d5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084423"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="0db66-103">IXml2Dex::CreateGraphFromFile (método)</span><span class="sxs-lookup"><span data-stu-id="0db66-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="0db66-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0db66-104">\[Deprecated.</span></span> <span data-ttu-id="0db66-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0db66-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0db66-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="0db66-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db66-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0db66-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="0db66-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0db66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db66-109">*ppGraph*</span><span class="sxs-lookup"><span data-stu-id="0db66-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="0db66-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0db66-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0db66-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="0db66-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="0db66-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0db66-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0db66-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="0db66-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="0db66-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0db66-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db66-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0db66-115">Return value</span></span>

<span data-ttu-id="0db66-116">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0db66-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0db66-117">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0db66-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0db66-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0db66-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0db66-119">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="0db66-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0db66-120">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0db66-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0db66-121">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0db66-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0db66-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0db66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db66-123">**IXml2Dex (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="0db66-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



