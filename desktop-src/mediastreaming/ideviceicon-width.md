---
title: IDeviceIcon width, método
description: Recupera el ancho del icono en píxeles.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Width (método) API de streaming de multimedia
- Método width API de streaming de multimedia, interfaz IDeviceIcon
- IDeviceIcon interface media streaming API, width (método)
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358956"
---
# <a name="ideviceiconwidth-method"></a><span data-ttu-id="57123-106">IDeviceIcon:: width (método)</span><span class="sxs-lookup"><span data-stu-id="57123-106">IDeviceIcon::Width method</span></span>

<span data-ttu-id="57123-107">Recupera el ancho del icono en píxeles.</span><span class="sxs-lookup"><span data-stu-id="57123-107">Retrieves the width of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="57123-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57123-108">Syntax</span></span>


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="57123-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57123-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57123-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57123-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57123-111">Recibe un puntero al ancho del icono en píxeles.</span><span class="sxs-lookup"><span data-stu-id="57123-111">Receives a pointer to the width of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57123-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57123-112">Return value</span></span>

<span data-ttu-id="57123-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="57123-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="57123-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="57123-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="57123-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="57123-115">Return code</span></span>                                                                          | <span data-ttu-id="57123-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="57123-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="57123-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="57123-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="57123-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="57123-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="57123-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="57123-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57123-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="57123-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

