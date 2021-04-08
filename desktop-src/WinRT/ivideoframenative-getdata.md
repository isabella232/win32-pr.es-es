---
description: Este método devuelve una interfaz que proporciona acceso a los datos de vídeo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'IVideoFrameNative:: GetData (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001147"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="7624d-103">IVideoFrameNative:: GetData (método)</span><span class="sxs-lookup"><span data-stu-id="7624d-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="7624d-104">Este método devuelve una interfaz que proporciona acceso a los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7624d-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7624d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7624d-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="7624d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7624d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7624d-107">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7624d-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7624d-108">IID de la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="7624d-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7624d-109">*PPV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7624d-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7624d-110">Cuando este método se devuelve correctamente, contiene el puntero de interfaz solicitado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="7624d-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7624d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7624d-111">Return value</span></span>

<span data-ttu-id="7624d-112">Devuelve S \_ correcto al finalizar correctamente.</span><span class="sxs-lookup"><span data-stu-id="7624d-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="7624d-113">Devuelve E \_ nointerface si no se encuentra la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="7624d-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="7624d-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7624d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7624d-115">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="7624d-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



