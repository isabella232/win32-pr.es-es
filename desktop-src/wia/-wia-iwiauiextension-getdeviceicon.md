---
description: Obtiene un icono de dispositivo personalizado.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension:: GetDeviceIcon (método) (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154391"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="b55d4-103">IWiaUIExtension:: GetDeviceIcon (método)</span><span class="sxs-lookup"><span data-stu-id="b55d4-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="b55d4-104">Obtiene un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b55d4-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b55d4-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="b55d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b55d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b55d4-107">*bstrDeviceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b55d4-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b55d4-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b55d4-108">Type: **BSTR**</span></span>

<span data-ttu-id="b55d4-109">Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.</span><span class="sxs-lookup"><span data-stu-id="b55d4-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="b55d4-110">*phIcon* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b55d4-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b55d4-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="b55d4-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="b55d4-112">Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b55d4-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="b55d4-113">_nSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b55d4-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b55d4-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="b55d4-114">Type: **ULONG**</span></span>

<span data-ttu-id="b55d4-115">Especifica el tamaño de icono deseado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b55d4-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="b55d4-116">Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.</span><span class="sxs-lookup"><span data-stu-id="b55d4-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b55d4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b55d4-117">Return value</span></span>

<span data-ttu-id="b55d4-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b55d4-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b55d4-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b55d4-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b55d4-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b55d4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b55d4-121">Requirements</span></span>



| <span data-ttu-id="b55d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b55d4-122">Requirement</span></span> | <span data-ttu-id="b55d4-123">Value</span><span class="sxs-lookup"><span data-stu-id="b55d4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b55d4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b55d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b55d4-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b55d4-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b55d4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b55d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b55d4-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b55d4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b55d4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b55d4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b55d4-129"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55d4-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




