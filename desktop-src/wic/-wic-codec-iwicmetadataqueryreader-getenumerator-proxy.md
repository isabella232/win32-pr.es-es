---
description: Función de proxy para el método GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678321"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="d8dbe-103">IWICMetadataQueryReader \_ GetEnumerator ( \_ función de proxy)</span><span class="sxs-lookup"><span data-stu-id="d8dbe-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="d8dbe-104">Función de proxy para el método [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .</span><span class="sxs-lookup"><span data-stu-id="d8dbe-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8dbe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8dbe-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="d8dbe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8dbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8dbe-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d8dbe-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dbe-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="d8dbe-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="d8dbe-109">Puntero a este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="d8dbe-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="d8dbe-110">*ppIEnumString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8dbe-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dbe-111">Tipo: **IEnumString \* \***</span><span class="sxs-lookup"><span data-stu-id="d8dbe-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="d8dbe-112">Puntero que recibe un puntero a un enumerador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="d8dbe-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8dbe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8dbe-113">Return value</span></span>

<span data-ttu-id="d8dbe-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8dbe-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d8dbe-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d8dbe-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8dbe-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8dbe-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8dbe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8dbe-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8dbe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8dbe-118">Requirements</span></span>



| <span data-ttu-id="d8dbe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8dbe-119">Requirement</span></span> | <span data-ttu-id="d8dbe-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8dbe-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dbe-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8dbe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8dbe-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8dbe-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8dbe-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8dbe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8dbe-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8dbe-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8dbe-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8dbe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8dbe-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8dbe-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




