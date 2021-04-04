---
title: IDRMStatusCallback método de estado
description: El método de estado recibe mensajes de estado de los procesos DRM asíncronos.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Método de estado Windows Media Format
- Método OnFormat formato de Windows Media, interfaz IDRMStatusCallback
- Interfaz IDRMStatusCallback formato de Windows Media, método de estado
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076608"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="a0ccb-106">IDRMStatusCallback:: alstatus (método)</span><span class="sxs-lookup"><span data-stu-id="a0ccb-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="a0ccb-107">El método de **Estado** recibe mensajes de estado de los procesos DRM asíncronos.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ccb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0ccb-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="a0ccb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0ccb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ccb-110">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a0ccb-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ccb-111">Código de estado.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-111">Status code.</span></span> <span data-ttu-id="a0ccb-112">Los códigos de mensaje se definen en el tipo de enumeración de **\_ Estado MSDRM** .</span><span class="sxs-lookup"><span data-stu-id="a0ccb-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a0ccb-113">*HR* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0ccb-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ccb-114">Código de retorno que admite el mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="a0ccb-115">*dwType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0ccb-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ccb-116">Tipo de los datos a los que señala *pValue*.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="a0ccb-117">Establezca en uno de los valores de la enumeración de [**\_ tipos de tipo de \_ texto DRM ATTR**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ccb-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a0ccb-118">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0ccb-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ccb-119">Puntero a los datos relacionados con el mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="a0ccb-120">El tipo de datos viene determinado por el valor del parámetro *dwType* .</span><span class="sxs-lookup"><span data-stu-id="a0ccb-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="a0ccb-121">Para obtener más información, consulte la enumeración del [**\_ \_ tipo de datos DRM ATTR**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ccb-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a0ccb-122">*pvContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0ccb-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ccb-123">Parámetro opcional que se puede utilizar para identificar el objeto que envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="a0ccb-124">Al establecer *pvContext* al registrar esta devolución de llamada, puede usar la misma devolución de llamada para controlar varios procesos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ccb-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0ccb-125">Return value</span></span>

<span data-ttu-id="a0ccb-126">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a0ccb-127">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a0ccb-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a0ccb-128">Return code</span></span>                                                                          | <span data-ttu-id="a0ccb-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0ccb-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a0ccb-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a0ccb-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a0ccb-131">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0ccb-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0ccb-132">Remarks</span></span>

<span data-ttu-id="a0ccb-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a0ccb-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0ccb-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a0ccb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ccb-135">**TIPO de los atributos de DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a0ccb-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="a0ccb-136">**Interfaz IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="a0ccb-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





