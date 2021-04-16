---
title: IMediaRenderer IsImageSupported, método
description: Recupera un valor que indica si el DMR es capaz de mostrar imágenes.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- Método IsImageSupported API de streaming de multimedia
- Método IsImageSupported API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714299"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="152de-106">IMediaRenderer:: IsImageSupported (método)</span><span class="sxs-lookup"><span data-stu-id="152de-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="152de-107">Recupera un valor que indica si el DMR es capaz de mostrar imágenes.</span><span class="sxs-lookup"><span data-stu-id="152de-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="152de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="152de-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="152de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="152de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152de-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="152de-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="152de-111">Valor booleano que es **true** si el DMR es capaz de mostrar imágenes y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="152de-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152de-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="152de-112">Return value</span></span>

<span data-ttu-id="152de-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="152de-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="152de-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="152de-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="152de-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="152de-115">Return code</span></span>                                                                          | <span data-ttu-id="152de-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="152de-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="152de-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="152de-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="152de-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="152de-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="152de-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="152de-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152de-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="152de-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





