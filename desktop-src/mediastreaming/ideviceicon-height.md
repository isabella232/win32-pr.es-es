---
title: IDeviceIcon (método) height
description: Recupera el alto del icono en píxeles.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Height (método) API de streaming de multimedia
- Height (método) API de streaming de multimedia, interfaz IDeviceIcon
- IDeviceIcon interface media streaming API, Height (método)
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdba8d107cc844a29d215e5da49949595a8cd27a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077741"
---
# <a name="ideviceiconheight-method"></a><span data-ttu-id="75f48-106">IDeviceIcon:: Height (método)</span><span class="sxs-lookup"><span data-stu-id="75f48-106">IDeviceIcon::Height method</span></span>

<span data-ttu-id="75f48-107">Recupera el alto del icono en píxeles.</span><span class="sxs-lookup"><span data-stu-id="75f48-107">Retrieves the height of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f48-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75f48-108">Syntax</span></span>


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="75f48-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75f48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f48-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75f48-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75f48-111">Recibe un puntero al alto del icono en píxeles.</span><span class="sxs-lookup"><span data-stu-id="75f48-111">Receives a pointer to the height of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f48-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75f48-112">Return value</span></span>

<span data-ttu-id="75f48-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75f48-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75f48-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="75f48-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75f48-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75f48-115">Return code</span></span>                                                                          | <span data-ttu-id="75f48-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="75f48-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="75f48-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="75f48-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="75f48-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="75f48-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="75f48-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="75f48-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f48-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="75f48-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

