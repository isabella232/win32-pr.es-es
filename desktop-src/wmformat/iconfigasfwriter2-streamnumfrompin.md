---
title: IConfigAsfWriter2 StreamNumFromPin, método
description: El método StreamNumFromPin recupera el número de secuencia asociado al pin de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Método StreamNumFromPin formato de Windows Media
- Método StreamNumFromPin formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420850"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="65a4e-106">IConfigAsfWriter2:: StreamNumFromPin (método)</span><span class="sxs-lookup"><span data-stu-id="65a4e-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="65a4e-107">El método **StreamNumFromPin** recupera el número de secuencia asociado al pin de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="65a4e-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a4e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65a4e-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="65a4e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65a4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a4e-110">*pPin* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a4e-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4e-111">Puntero a la interfaz **IPin** en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="65a4e-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="65a4e-112">*pwStreamNum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65a4e-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a4e-113">Puntero que recibe el número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="65a4e-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a4e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65a4e-114">Return value</span></span>

<span data-ttu-id="65a4e-115">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="65a4e-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="65a4e-116">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65a4e-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a4e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65a4e-117">Remarks</span></span>

<span data-ttu-id="65a4e-118">En ocasiones, puede que necesite usar las interfaces del SDK de Windows Media Format directamente para manipular un flujo antes de ejecutar un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="65a4e-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="65a4e-119">Dado que no se puede suponer que un número de secuencia ASF es el mismo que el número de PIN de DirectShow, se proporciona este método.</span><span class="sxs-lookup"><span data-stu-id="65a4e-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="65a4e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="65a4e-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="65a4e-121">[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65a4e-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 