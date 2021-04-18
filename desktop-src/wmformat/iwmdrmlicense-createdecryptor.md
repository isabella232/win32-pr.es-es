---
title: Método CreateDecryptor IWMDRMLicense (wmdrmsdk. h)
description: El método CreateDecryptor crea un objeto descifrador con la configuración de la licencia actual.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- CreateDecryptor (método) formato de Windows Media
- Método CreateDecryptor Windows Media Format, IWMDRMLicense (interfaz)
- Interfaz IWMDRMLicense formato de Windows Media, método CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660150"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="bb910-106">IWMDRMLicense:: CreateDecryptor (método)</span><span class="sxs-lookup"><span data-stu-id="bb910-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="bb910-107">El método **CreateDecryptor** crea un objeto descifrador con la configuración de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="bb910-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb910-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb910-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="bb910-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb910-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb910-110">*ppDecryptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb910-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb910-111">Recibe un puntero a la interfaz [**IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="bb910-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb910-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb910-112">Return value</span></span>

<span data-ttu-id="bb910-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bb910-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb910-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="bb910-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb910-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bb910-115">Return code</span></span>                                                                                                | <span data-ttu-id="bb910-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb910-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bb910-117"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="bb910-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="bb910-118">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="bb910-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="bb910-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bb910-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="bb910-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="bb910-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="bb910-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb910-121">Remarks</span></span>

<span data-ttu-id="bb910-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb910-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb910-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb910-123">Requirements</span></span>



| <span data-ttu-id="bb910-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb910-124">Requirement</span></span> | <span data-ttu-id="bb910-125">Value</span><span class="sxs-lookup"><span data-stu-id="bb910-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb910-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb910-126">Header</span></span><br/> | <dl> <span data-ttu-id="bb910-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb910-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb910-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb910-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb910-129">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="bb910-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="bb910-130">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="bb910-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





