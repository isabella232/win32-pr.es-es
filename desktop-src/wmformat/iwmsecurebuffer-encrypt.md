---
title: Método Encrypt de IWMSecureBuffer (wmdrmsdk. h)
description: El método Encrypt cifra un puntero de datos.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Método de cifrado de Windows Media Format
- Método Encrypt formato de Windows Media, interfaz IWMSecureBuffer
- Interfaz IWMSecureBuffer formato de Windows Media, método Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709249"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="80c82-106">IWMSecureBuffer:: Encrypt (método)</span><span class="sxs-lookup"><span data-stu-id="80c82-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="80c82-107">El método **Encrypt** cifra un puntero de datos.</span><span class="sxs-lookup"><span data-stu-id="80c82-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c82-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80c82-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="80c82-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80c82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c82-110">*pSecureChannel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80c82-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c82-111">Puntero a una interfaz de canal seguro que contiene el puntero de datos que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="80c82-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c82-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80c82-112">Return value</span></span>

<span data-ttu-id="80c82-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="80c82-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="80c82-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="80c82-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="80c82-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="80c82-115">Return code</span></span>                                                                          | <span data-ttu-id="80c82-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="80c82-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="80c82-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="80c82-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="80c82-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="80c82-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80c82-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80c82-119">Remarks</span></span>

<span data-ttu-id="80c82-120">Utilice este método para cifrar los punteros de datos de manera que se puedan enviar a través de límites de DLL.</span><span class="sxs-lookup"><span data-stu-id="80c82-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c82-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c82-121">Requirements</span></span>



| <span data-ttu-id="80c82-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c82-122">Requirement</span></span> | <span data-ttu-id="80c82-123">Value</span><span class="sxs-lookup"><span data-stu-id="80c82-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80c82-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80c82-124">Header</span></span><br/>  | <dl> <span data-ttu-id="80c82-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c82-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="80c82-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80c82-126">Library</span></span><br/> | <dl> <span data-ttu-id="80c82-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80c82-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c82-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="80c82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c82-129">**Descifrado**</span><span class="sxs-lookup"><span data-stu-id="80c82-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="80c82-130">**Interfaz IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="80c82-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





