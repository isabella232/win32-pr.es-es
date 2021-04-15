---
title: IConfigAsfWriter2 ResetMultiPassState, método
description: El método ResetMultiPassState restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Método ResetMultiPassState formato de Windows Media
- Método ResetMultiPassState formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421202"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="a8ada-106">IConfigAsfWriter2:: ResetMultiPassState (método)</span><span class="sxs-lookup"><span data-stu-id="a8ada-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="a8ada-107">El método **ResetMultiPassState** restablece el filtro cuando se cancela un paso de codificación de preprocesamiento antes de que se complete.</span><span class="sxs-lookup"><span data-stu-id="a8ada-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ada-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8ada-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="a8ada-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8ada-109">Parameters</span></span>

<span data-ttu-id="a8ada-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8ada-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8ada-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8ada-111">Return value</span></span>

<span data-ttu-id="a8ada-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a8ada-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a8ada-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="a8ada-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a8ada-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8ada-114">Return code</span></span>                                                                                         | <span data-ttu-id="a8ada-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8ada-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="a8ada-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a8ada-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="a8ada-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="a8ada-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="a8ada-118"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="a8ada-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="a8ada-119">El filtro no se encontraba en un estado detenido.</span><span class="sxs-lookup"><span data-stu-id="a8ada-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8ada-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8ada-120">Remarks</span></span>

<span data-ttu-id="a8ada-121">Se debe llamar a este método para restablecer el estado interno del filtro siempre que se cancele un paso de codificación de preprocesamiento antes de que el filtro haya recibido un evento de **\_ \_ preprocesamiento de EC** .</span><span class="sxs-lookup"><span data-stu-id="a8ada-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="a8ada-122">No es necesario llamar a este método si la fase de codificación de preprocesamiento se completa sin errores.</span><span class="sxs-lookup"><span data-stu-id="a8ada-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8ada-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8ada-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8ada-124">[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8ada-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

