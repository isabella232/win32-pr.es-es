---
description: 'IWICMetadataQueryReader_GetContainerFormat_Proxy función: función proxy para el método GetContainerFormat.'
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097143"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="00334-103">Función IWICMetadataQueryReader \_ GetContainerFormat \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="00334-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="00334-104">Función de proxy para [**el método GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="00334-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00334-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00334-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="00334-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00334-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00334-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="00334-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00334-108">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="00334-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="00334-109">Puntero a este [**objeto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="00334-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="00334-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00334-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00334-111">Tipo: **\* GUID**</span><span class="sxs-lookup"><span data-stu-id="00334-111">Type: **GUID\***</span></span>

<span data-ttu-id="00334-112">Puntero que recibe el GUID de formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="00334-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00334-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00334-113">Return value</span></span>

<span data-ttu-id="00334-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00334-114">Type: **HRESULT**</span></span>

<span data-ttu-id="00334-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="00334-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00334-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="00334-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00334-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00334-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="00334-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00334-118">Requirements</span></span>



| <span data-ttu-id="00334-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00334-119">Requirement</span></span> | <span data-ttu-id="00334-120">Valor</span><span class="sxs-lookup"><span data-stu-id="00334-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00334-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00334-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00334-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00334-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="00334-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00334-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00334-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00334-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="00334-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00334-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00334-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="00334-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




