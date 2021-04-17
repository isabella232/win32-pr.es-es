---
description: Función de proxy para crear el IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706484"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="686b9-103">\_Función de proxy WICCreateImagingFactory</span><span class="sxs-lookup"><span data-stu-id="686b9-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="686b9-104">Función de proxy para crear el [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="686b9-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="686b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="686b9-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="686b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="686b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686b9-107">*SDKVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="686b9-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="686b9-108">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="686b9-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="686b9-109">*ppIImagingFactory* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="686b9-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="686b9-110">Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="686b9-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686b9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="686b9-111">Return value</span></span>

<span data-ttu-id="686b9-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="686b9-112">Type: **HRESULT**</span></span>

<span data-ttu-id="686b9-113">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="686b9-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="686b9-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="686b9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="686b9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="686b9-115">Remarks</span></span>

<span data-ttu-id="686b9-116">Esta función es una aplicación auxiliar para crear un generador WIC para la vinculación de DLL explícita, que era necesaria para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="686b9-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="686b9-117">En el uso normal, se usaría [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en su lugar (consulte generadores de clases de la [API de WIC](./-wic-api.md#class-factories)), ya que siempre se incluye en todas las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="686b9-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="686b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="686b9-118">Requirements</span></span>



| <span data-ttu-id="686b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="686b9-119">Requirement</span></span> | <span data-ttu-id="686b9-120">Value</span><span class="sxs-lookup"><span data-stu-id="686b9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686b9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="686b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="686b9-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="686b9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="686b9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="686b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="686b9-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="686b9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="686b9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="686b9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="686b9-126"><dt>Windowscodecs.dll; </dt> <dt>WindowsCodecs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="686b9-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

