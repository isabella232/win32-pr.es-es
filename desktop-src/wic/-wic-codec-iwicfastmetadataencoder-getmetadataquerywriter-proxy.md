---
description: Función de proxy para el método GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716791"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="62726-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="62726-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="62726-104">Función de proxy para el método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="62726-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62726-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62726-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="62726-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62726-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62726-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="62726-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62726-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="62726-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="62726-109">Puntero a este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="62726-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="62726-110">*ppIMetadataQueryWriter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="62726-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62726-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="62726-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="62726-112">Puntero que recibe un puntero al escritor de consultas de metadatos del codificador.</span><span class="sxs-lookup"><span data-stu-id="62726-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62726-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62726-113">Return value</span></span>

<span data-ttu-id="62726-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="62726-114">Type: **HRESULT**</span></span>

<span data-ttu-id="62726-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="62726-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62726-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62726-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62726-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62726-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="62726-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62726-118">Requirements</span></span>



| <span data-ttu-id="62726-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62726-119">Requirement</span></span> | <span data-ttu-id="62726-120">Value</span><span class="sxs-lookup"><span data-stu-id="62726-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62726-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62726-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62726-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62726-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="62726-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62726-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62726-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="62726-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="62726-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62726-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62726-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62726-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




