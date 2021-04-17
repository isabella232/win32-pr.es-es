---
title: Método IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: El método EncryptScatter descodifica y cifra los datos.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Método EncryptScatter formato de Windows Media
- Método EncryptScatter formato de Windows Media, interfaz IWMDRMEncryptScatter
- Interfaz IWMDRMEncryptScatter formato de Windows Media, método EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660151"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="82a97-106">IWMDRMEncryptScatter:: EncryptScatter (método)</span><span class="sxs-lookup"><span data-stu-id="82a97-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="82a97-107">El método **EncryptScatter** descodifica y cifra los datos.</span><span class="sxs-lookup"><span data-stu-id="82a97-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82a97-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="82a97-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82a97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a97-110">*cBlocks* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82a97-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a97-111">Número de elementos de la matriz *rgBlocks* .</span><span class="sxs-lookup"><span data-stu-id="82a97-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="82a97-112">*rgBlocks* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82a97-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a97-113">Matriz de una o varias estructuras de [**\_ bloques de \_ dispersión \_ de cifrado WMDRM**](wmdrm-encrypt-scatter-block.md) .</span><span class="sxs-lookup"><span data-stu-id="82a97-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="82a97-114">Cada elemento describe un bloque de datos que se va a descodificar y cifrar.</span><span class="sxs-lookup"><span data-stu-id="82a97-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="82a97-115">*pWMCryptoData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82a97-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a97-116">Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene los parámetros de cifrado.</span><span class="sxs-lookup"><span data-stu-id="82a97-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="82a97-117">Establezca en **null** para usar los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="82a97-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="82a97-118">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82a97-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a97-119">Tamaño del búfer de datos de salida pasado como *pbOutput*.</span><span class="sxs-lookup"><span data-stu-id="82a97-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="82a97-120">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82a97-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82a97-121">Búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="82a97-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a97-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82a97-122">Return value</span></span>

<span data-ttu-id="82a97-123">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="82a97-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82a97-124">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="82a97-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82a97-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="82a97-125">Return code</span></span>                                                                          | <span data-ttu-id="82a97-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="82a97-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="82a97-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="82a97-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="82a97-128">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="82a97-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82a97-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82a97-129">Remarks</span></span>

<span data-ttu-id="82a97-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82a97-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a97-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82a97-131">Requirements</span></span>



| <span data-ttu-id="82a97-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="82a97-132">Requirement</span></span> | <span data-ttu-id="82a97-133">Value</span><span class="sxs-lookup"><span data-stu-id="82a97-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82a97-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82a97-134">Header</span></span><br/> | <dl> <span data-ttu-id="82a97-135"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a97-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a97-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="82a97-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a97-137">**InitEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="82a97-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="82a97-138">**Interfaz IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="82a97-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





