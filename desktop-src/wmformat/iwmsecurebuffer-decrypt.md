---
title: Método de descifrado IWMSecureBuffer (wmdrmsdk. h)
description: El método de descifrado descifra un puntero de datos que se cifró llamando al método Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Método de descifrado formato de Windows Media
- Método de descifrado formato de Windows Media, interfaz IWMSecureBuffer
- Interfaz IWMSecureBuffer formato de Windows Media, descifrar método
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671808"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="72f55-106">IWMSecureBuffer::D método ECRYPT</span><span class="sxs-lookup"><span data-stu-id="72f55-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="72f55-107">El método de **descifrado** descifra un puntero de datos que se cifró llamando al método [**Encrypt**](iwmsecurebuffer-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="72f55-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f55-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72f55-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="72f55-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72f55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f55-110">*pSecureChannel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f55-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f55-111">Puntero a una interfaz de canal seguro que contiene el puntero de datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="72f55-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f55-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72f55-112">Return value</span></span>

<span data-ttu-id="72f55-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="72f55-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="72f55-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="72f55-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="72f55-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="72f55-115">Return code</span></span>                                                                          | <span data-ttu-id="72f55-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="72f55-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="72f55-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="72f55-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="72f55-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="72f55-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72f55-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72f55-119">Remarks</span></span>

<span data-ttu-id="72f55-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72f55-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f55-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72f55-121">Requirements</span></span>



| <span data-ttu-id="72f55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f55-122">Requirement</span></span> | <span data-ttu-id="72f55-123">Value</span><span class="sxs-lookup"><span data-stu-id="72f55-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72f55-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72f55-124">Header</span></span><br/>  | <dl> <span data-ttu-id="72f55-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f55-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f55-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72f55-126">Library</span></span><br/> | <dl> <span data-ttu-id="72f55-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72f55-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f55-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f55-129">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="72f55-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="72f55-130">**Interfaz IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="72f55-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





