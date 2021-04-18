---
description: Función de proxy para el método SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716663"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="dc7df-103">IWICMetadataQueryWriter \_ SetMetadataByName \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="dc7df-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="dc7df-104">Función de proxy para el método [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="dc7df-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc7df-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="dc7df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7df-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dc7df-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7df-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="dc7df-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="dc7df-109">Puntero a este objeto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="dc7df-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="dc7df-110">*wzName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc7df-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7df-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="dc7df-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="dc7df-112">Nombre del elemento de metadatos.</span><span class="sxs-lookup"><span data-stu-id="dc7df-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="dc7df-113">*pvarValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc7df-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7df-114">Tipo: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="dc7df-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="dc7df-115">Los metadatos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="dc7df-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7df-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7df-116">Return value</span></span>

<span data-ttu-id="dc7df-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dc7df-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dc7df-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="dc7df-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc7df-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc7df-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc7df-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc7df-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7df-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc7df-121">Requirements</span></span>



| <span data-ttu-id="dc7df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc7df-122">Requirement</span></span> | <span data-ttu-id="dc7df-123">Value</span><span class="sxs-lookup"><span data-stu-id="dc7df-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7df-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc7df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7df-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc7df-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dc7df-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc7df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7df-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc7df-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dc7df-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc7df-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc7df-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc7df-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

