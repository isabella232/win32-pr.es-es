---
title: IDeviceIcon (método de ContentType)
description: Recupera el tipo de contenido del icono.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- ContentType (método) API de streaming de multimedia
- Método ContentType API de transmisión por secuencias de multimedia, interfaz IDeviceIcon
- IDeviceIcon interface media streaming API, ContentType (método)
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904527"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="1e229-106">IDeviceIcon:: ContentType (método)</span><span class="sxs-lookup"><span data-stu-id="1e229-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="1e229-107">Recupera el tipo de contenido del icono.</span><span class="sxs-lookup"><span data-stu-id="1e229-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e229-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e229-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="1e229-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e229-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e229-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1e229-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e229-111">Recibe un puntero al tipo de contenido del icono.</span><span class="sxs-lookup"><span data-stu-id="1e229-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e229-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e229-112">Return value</span></span>

<span data-ttu-id="1e229-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1e229-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1e229-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="1e229-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1e229-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1e229-115">Return code</span></span>                                                                          | <span data-ttu-id="1e229-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e229-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1e229-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1e229-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1e229-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1e229-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1e229-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e229-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e229-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="1e229-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

