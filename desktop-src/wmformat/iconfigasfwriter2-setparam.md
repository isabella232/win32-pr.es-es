---
title: IConfigAsfWriter2 SetParam, método
description: El método SetParam establece el valor del parámetro de configuración de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Método SetParam formato de Windows Media
- Método SetParam formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695692"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="be13f-106">IConfigAsfWriter2:: SetParam (método)</span><span class="sxs-lookup"><span data-stu-id="be13f-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="be13f-107">El método **SetParam** establece el valor del parámetro de configuración de filtro especificado.</span><span class="sxs-lookup"><span data-stu-id="be13f-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="be13f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be13f-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="be13f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be13f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be13f-110">*dwParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be13f-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be13f-111">Especifica el parámetro que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="be13f-111">Specifies the parameter to set.</span></span> <span data-ttu-id="be13f-112">Debe ser un valor definido en la enumeración de [ \_ \_ \_ parámetros AM ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be13f-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="be13f-113">*dwParam1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be13f-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be13f-114">Especifica el valor que se va a asignar al parámetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="be13f-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="be13f-115">*dwParam2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be13f-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be13f-116">No se utiliza; debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="be13f-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be13f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be13f-117">Return value</span></span>

<span data-ttu-id="be13f-118">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="be13f-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="be13f-119">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be13f-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="be13f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="be13f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="be13f-121">[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be13f-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="be13f-122">**IConfigAsfWriter2:: GetParam**</span><span class="sxs-lookup"><span data-stu-id="be13f-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 