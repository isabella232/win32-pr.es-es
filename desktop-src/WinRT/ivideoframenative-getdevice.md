---
description: Este método devuelve un dispositivo asociado a los datos de vídeo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'IVideoFrameNative:: GetDevice (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423784"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="81277-103">IVideoFrameNative:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="81277-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="81277-104">Este método devuelve un dispositivo asociado a los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="81277-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="81277-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81277-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="81277-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81277-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81277-107">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81277-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81277-108">IID del dispositivo que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="81277-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="81277-109">*PPV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="81277-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81277-110">Cuando este método se devuelve correctamente, contiene el puntero de dispositivo solicitado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="81277-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81277-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81277-111">Return value</span></span>

<span data-ttu-id="81277-112">Devuelve S \_ correcto al finalizar correctamente.</span><span class="sxs-lookup"><span data-stu-id="81277-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="81277-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="81277-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81277-114">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="81277-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



