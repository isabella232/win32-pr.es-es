---
description: Obtiene un logotipo de mapa de bits personalizado para el dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension:: GetDeviceBitmapLogo (método) (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696516"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="6e260-103">IWiaUIExtension:: GetDeviceBitmapLogo (método)</span><span class="sxs-lookup"><span data-stu-id="6e260-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="6e260-104">Obtiene un logotipo de mapa de bits personalizado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e260-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e260-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e260-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="6e260-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e260-107">*bstrDeviceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e260-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e260-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6e260-108">Type: **BSTR**</span></span>

<span data-ttu-id="6e260-109">Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.</span><span class="sxs-lookup"><span data-stu-id="6e260-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="6e260-110">*phBitmap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e260-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e260-111">Tipo: \**hBitmap \** _</span><span class="sxs-lookup"><span data-stu-id="6e260-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="6e260-112">Apunta a una ubicación de memoria que recibirá un identificador para el logotipo de mapa de bits para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e260-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="6e260-113">_nMaxWidth \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6e260-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e260-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="6e260-114">Type: **ULONG**</span></span>

<span data-ttu-id="6e260-115">Especifica el ancho deseado del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6e260-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="6e260-116">*nMaxHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e260-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e260-117">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="6e260-117">Type: **ULONG**</span></span>

<span data-ttu-id="6e260-118">Especifica el alto deseado del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6e260-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e260-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e260-119">Return value</span></span>

<span data-ttu-id="6e260-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e260-120">Type: **HRESULT**</span></span>

<span data-ttu-id="6e260-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6e260-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e260-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e260-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e260-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e260-123">Requirements</span></span>



| <span data-ttu-id="6e260-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e260-124">Requirement</span></span> | <span data-ttu-id="6e260-125">Value</span><span class="sxs-lookup"><span data-stu-id="6e260-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e260-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e260-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6e260-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6e260-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6e260-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e260-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6e260-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e260-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e260-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e260-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e260-131"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e260-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




