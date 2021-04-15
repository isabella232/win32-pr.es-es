---
title: IConfigAsfWriter2 GetParam, método
description: El método GetParam recupera el valor actual del parámetro de configuración de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Método GetParam formato de Windows Media
- Método GetParam formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695712"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="906f3-106">IConfigAsfWriter2:: GetParam (método)</span><span class="sxs-lookup"><span data-stu-id="906f3-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="906f3-107">El método **GetParam** recupera el valor actual del parámetro de configuración de filtro especificado.</span><span class="sxs-lookup"><span data-stu-id="906f3-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="906f3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="906f3-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="906f3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="906f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906f3-110">*dwParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="906f3-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f3-111">Especifica el parámetro que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="906f3-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="906f3-112">Debe ser un valor definido en la enumeración de [ \_ \_ \_ parámetros AM ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="906f3-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="906f3-113">*pdwParam1* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="906f3-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="906f3-114">Puntero a una variable que recupera el valor del parámetro especificado en *dwParam*.</span><span class="sxs-lookup"><span data-stu-id="906f3-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="906f3-115">*pdwParam2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="906f3-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="906f3-116">No se utiliza, debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="906f3-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906f3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="906f3-117">Return value</span></span>

<span data-ttu-id="906f3-118">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="906f3-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="906f3-119">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="906f3-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="906f3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="906f3-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="906f3-121">[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="906f3-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="906f3-122">**IConfigAsfWriter2::SetParam**</span><span class="sxs-lookup"><span data-stu-id="906f3-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 