---
description: Función de proxy para el método RemoveMetadataByName.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: IWICMetadataQueryWriter_RemoveMetadataByName_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911149"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="b1a3d-103">IWICMetadataQueryWriter \_ RemoveMetadataByName \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="b1a3d-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="b1a3d-104">Función de proxy para el método [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="b1a3d-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1a3d-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="b1a3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1a3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a3d-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b1a3d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a3d-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="b1a3d-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="b1a3d-109">Puntero a este objeto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="b1a3d-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="b1a3d-110">*wzName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1a3d-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a3d-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b1a3d-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b1a3d-112">Nombre del elemento de metadatos que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="b1a3d-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a3d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1a3d-113">Return value</span></span>

<span data-ttu-id="b1a3d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1a3d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b1a3d-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b1a3d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1a3d-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1a3d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a3d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1a3d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a3d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a3d-118">Requirements</span></span>



| <span data-ttu-id="b1a3d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a3d-119">Requirement</span></span> | <span data-ttu-id="b1a3d-120">Value</span><span class="sxs-lookup"><span data-stu-id="b1a3d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a3d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1a3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a3d-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1a3d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b1a3d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1a3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a3d-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1a3d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b1a3d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1a3d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1a3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




