---
title: IDeviceIcon (método de secuencia)
description: Recupera el icono como un flujo.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Streaming de media streaming API
- Streaming de media streaming API, interfaz IDeviceIcon
- Interfaz IDeviceIcon API de streaming de multimedia, método de secuencia
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358957"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="9dd2d-106">IDeviceIcon:: Stream (método)</span><span class="sxs-lookup"><span data-stu-id="9dd2d-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="9dd2d-107">Recupera el icono como un flujo.</span><span class="sxs-lookup"><span data-stu-id="9dd2d-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd2d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dd2d-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="9dd2d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dd2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd2d-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9dd2d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd2d-111">Recibe una referencia a un [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) que se puede usar para recuperar los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9dd2d-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd2d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dd2d-112">Return value</span></span>

<span data-ttu-id="9dd2d-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9dd2d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9dd2d-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9dd2d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9dd2d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9dd2d-115">Return code</span></span>                                                                          | <span data-ttu-id="9dd2d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dd2d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9dd2d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9dd2d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9dd2d-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9dd2d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9dd2d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dd2d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd2d-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="9dd2d-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

