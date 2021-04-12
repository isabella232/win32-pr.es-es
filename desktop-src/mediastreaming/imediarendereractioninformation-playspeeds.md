---
title: IMediaRendererActionInformation PlaySpeeds, método
description: Recupera la lista completa de valores de PlaySpeed que acepta el DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Método PlaySpeeds API de streaming de multimedia
- Método PlaySpeeds API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358924"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="efbcc-106">IMediaRendererActionInformation::P método laySpeeds</span><span class="sxs-lookup"><span data-stu-id="efbcc-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="efbcc-107">Recupera la lista completa de valores de [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que acepta el DMR.</span><span class="sxs-lookup"><span data-stu-id="efbcc-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbcc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efbcc-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="efbcc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efbcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbcc-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="efbcc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efbcc-111">Recibe un vector de estructuras [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que especifica la lista completa de valores **PlaySpeed** aceptados por el DMR.</span><span class="sxs-lookup"><span data-stu-id="efbcc-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbcc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efbcc-112">Return value</span></span>

<span data-ttu-id="efbcc-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="efbcc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="efbcc-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="efbcc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="efbcc-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="efbcc-115">Return code</span></span>                                                                          | <span data-ttu-id="efbcc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="efbcc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="efbcc-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="efbcc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="efbcc-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="efbcc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="efbcc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="efbcc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbcc-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="efbcc-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

