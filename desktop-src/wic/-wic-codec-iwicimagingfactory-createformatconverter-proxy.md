---
description: Función de proxy para el método CreateFormatConverter.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278470"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="f3858-103">IWICImagingFactory \_ CreateFormatConverter \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="f3858-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="f3858-104">Función de proxy para el método [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="f3858-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3858-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3858-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="f3858-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3858-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3858-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3858-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3858-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f3858-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f3858-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3858-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3858-110">Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="f3858-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="f3858-111">Puntero que recibe un puntero a un nuevo [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span><span class="sxs-lookup"><span data-stu-id="f3858-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3858-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3858-112">Return value</span></span>

<span data-ttu-id="f3858-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f3858-113">Type: **HRESULT**</span></span>

<span data-ttu-id="f3858-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f3858-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3858-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3858-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3858-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3858-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3858-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3858-117">Requirements</span></span>



| <span data-ttu-id="f3858-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3858-118">Requirement</span></span> | <span data-ttu-id="f3858-119">Value</span><span class="sxs-lookup"><span data-stu-id="f3858-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3858-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3858-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3858-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3858-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f3858-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3858-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3858-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3858-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f3858-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3858-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3858-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3858-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




