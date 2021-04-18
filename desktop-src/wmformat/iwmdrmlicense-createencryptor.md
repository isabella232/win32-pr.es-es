---
title: Método CreateEncryptor de IWMDRMLicense (wmdrmsdk. h)
description: El método CreateEncryptor crea un objeto de sistema de cifrado con la configuración de la licencia actual.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Método CreateEncryptor formato de Windows Media
- Método CreateEncryptor formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método CreateEncryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708895"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="e92f8-106">IWMDRMLicense:: CreateEncryptor (método)</span><span class="sxs-lookup"><span data-stu-id="e92f8-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="e92f8-107">El método **CreateEncryptor** crea un objeto de sistema de cifrado con la configuración de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="e92f8-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="e92f8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e92f8-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="e92f8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e92f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e92f8-110">*ppEncryptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e92f8-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f8-111">Recibe un puntero a la interfaz [**IWMDRMEncrypt**](iwmdrmencrypt.md) del objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="e92f8-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e92f8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e92f8-112">Return value</span></span>

<span data-ttu-id="e92f8-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e92f8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e92f8-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e92f8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e92f8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e92f8-115">Return code</span></span>                                                                                                | <span data-ttu-id="e92f8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e92f8-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="e92f8-117"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="e92f8-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="e92f8-118">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="e92f8-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="e92f8-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e92f8-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e92f8-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e92f8-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e92f8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e92f8-121">Remarks</span></span>

<span data-ttu-id="e92f8-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e92f8-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e92f8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e92f8-123">Requirements</span></span>



| <span data-ttu-id="e92f8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e92f8-124">Requirement</span></span> | <span data-ttu-id="e92f8-125">Value</span><span class="sxs-lookup"><span data-stu-id="e92f8-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e92f8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e92f8-126">Header</span></span><br/> | <dl> <span data-ttu-id="e92f8-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e92f8-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e92f8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e92f8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92f8-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="e92f8-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="e92f8-130">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="e92f8-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





