---
title: Método Encrypt de IWMDRMEncrypt (wmdrmsdk. h)
description: El método Encrypt cifra un búfer de datos en contexto.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Método de cifrado de Windows Media Format
- Método Encrypt formato de Windows Media, interfaz IWMDRMEncrypt
- Interfaz IWMDRMEncrypt formato de Windows Media, método Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718611"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="6eb5b-106">IWMDRMEncrypt:: Encrypt (método)</span><span class="sxs-lookup"><span data-stu-id="6eb5b-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="6eb5b-107">El método **Encrypt** cifra un búfer de datos en contexto.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6eb5b-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="6eb5b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6eb5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eb5b-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6eb5b-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb5b-111">Datos que se van a cifrar.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-111">Data to encrypt.</span></span> <span data-ttu-id="6eb5b-112">Si el método se ejecuta correctamente, los datos se cifran en la devolución.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="6eb5b-113">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6eb5b-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb5b-114">Tamaño de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6eb5b-115">*pWMCryptoData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6eb5b-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb5b-116">Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="6eb5b-117">Establezca en **null** para usar los valores de cifrado predeterminados.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eb5b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6eb5b-118">Return value</span></span>

<span data-ttu-id="6eb5b-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6eb5b-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6eb5b-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6eb5b-121">Return code</span></span>                                                                          | <span data-ttu-id="6eb5b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6eb5b-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6eb5b-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6eb5b-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6eb5b-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6eb5b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6eb5b-125">Remarks</span></span>

<span data-ttu-id="6eb5b-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6eb5b-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb5b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb5b-127">Requirements</span></span>



| <span data-ttu-id="6eb5b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb5b-128">Requirement</span></span> | <span data-ttu-id="6eb5b-129">Value</span><span class="sxs-lookup"><span data-stu-id="6eb5b-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb5b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eb5b-130">Header</span></span><br/> | <dl> <span data-ttu-id="6eb5b-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb5b-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb5b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6eb5b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb5b-133">**Interfaz IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="6eb5b-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="6eb5b-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="6eb5b-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





