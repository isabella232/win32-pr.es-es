---
title: Método IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: El método InitEncryptScatter inicializa la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Método InitEncryptScatter formato de Windows Media
- Método InitEncryptScatter formato de Windows Media, interfaz IWMDRMEncryptScatter
- Interfaz IWMDRMEncryptScatter formato de Windows Media, método InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660652"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="64453-106">IWMDRMEncryptScatter:: InitEncryptScatter (método)</span><span class="sxs-lookup"><span data-stu-id="64453-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="64453-107">El método **InitEncryptScatter** inicializa la interfaz **IWMDRMEncryptScatter** para su uso.</span><span class="sxs-lookup"><span data-stu-id="64453-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="64453-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64453-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="64453-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64453-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64453-110">*cStreams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64453-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64453-111">Número de elementos de la matriz *rgInfos* .</span><span class="sxs-lookup"><span data-stu-id="64453-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="64453-112">Este es también el número de flujos que se incluyen en los datos que se van a cifrar.</span><span class="sxs-lookup"><span data-stu-id="64453-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="64453-113">*rgInfos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64453-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64453-114">Matriz de una o varias estructuras de [**\_ \_ \_ información de dispersión cifrada de WMDRM**](wmdrm-encrypt-scatter-info.md) .</span><span class="sxs-lookup"><span data-stu-id="64453-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="64453-115">Cada elemento contiene información de cifrado de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="64453-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="64453-116">El número de elementos de esta matriz debe ser igual al valor de *cStreams*.</span><span class="sxs-lookup"><span data-stu-id="64453-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64453-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64453-117">Return value</span></span>

<span data-ttu-id="64453-118">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="64453-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64453-119">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="64453-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64453-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="64453-120">Return code</span></span>                                                                          | <span data-ttu-id="64453-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="64453-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="64453-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="64453-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="64453-123">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="64453-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64453-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64453-124">Remarks</span></span>

<span data-ttu-id="64453-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="64453-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="64453-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64453-126">Requirements</span></span>



| <span data-ttu-id="64453-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="64453-127">Requirement</span></span> | <span data-ttu-id="64453-128">Value</span><span class="sxs-lookup"><span data-stu-id="64453-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64453-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64453-129">Header</span></span><br/> | <dl> <span data-ttu-id="64453-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="64453-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64453-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="64453-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64453-132">**EncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="64453-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="64453-133">**Interfaz IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="64453-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





