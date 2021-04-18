---
title: Método de descifrado IWMDRMDecrypt (wmdrmsdk. h)
description: El método de descifrado descifra un búfer de datos en contexto.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Método de descifrado formato de Windows Media
- Método de descifrado formato de Windows Media, interfaz IWMDRMDecrypt
- Interfaz IWMDRMDecrypt formato de Windows Media, descifrar método
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718612"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="51b97-106">IWMDRMDecrypt::D método ECRYPT</span><span class="sxs-lookup"><span data-stu-id="51b97-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="51b97-107">El método de **descifrado** descifra un búfer de datos en contexto.</span><span class="sxs-lookup"><span data-stu-id="51b97-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51b97-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="51b97-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51b97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51b97-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="51b97-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51b97-111">Datos que se van a descifrar.</span><span class="sxs-lookup"><span data-stu-id="51b97-111">Data to be decrypted.</span></span> <span data-ttu-id="51b97-112">Si el método se ejecuta correctamente, estos datos se descifran en la devolución.</span><span class="sxs-lookup"><span data-stu-id="51b97-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="51b97-113">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51b97-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b97-114">Tamaño de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="51b97-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="51b97-115">*pWMCryptoData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51b97-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51b97-116">Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros adicionales.</span><span class="sxs-lookup"><span data-stu-id="51b97-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="51b97-117">Puede ser **null** si el contenido se cifró con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="51b97-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51b97-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51b97-118">Return value</span></span>

<span data-ttu-id="51b97-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="51b97-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="51b97-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="51b97-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="51b97-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="51b97-121">Return code</span></span>                                                                          | <span data-ttu-id="51b97-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="51b97-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="51b97-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="51b97-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="51b97-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="51b97-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51b97-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51b97-125">Remarks</span></span>

<span data-ttu-id="51b97-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="51b97-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b97-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51b97-127">Requirements</span></span>



| <span data-ttu-id="51b97-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b97-128">Requirement</span></span> | <span data-ttu-id="51b97-129">Value</span><span class="sxs-lookup"><span data-stu-id="51b97-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51b97-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51b97-130">Header</span></span><br/> | <dl> <span data-ttu-id="51b97-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b97-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b97-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="51b97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b97-133">**Interfaz IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="51b97-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="51b97-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="51b97-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





