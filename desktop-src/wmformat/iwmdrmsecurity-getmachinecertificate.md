---
title: Método IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: El método GetMachineCertificate recupera el certificado de equipo del subsistema DRM en el equipo cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Método GetMachineCertificate formato de Windows Media
- Método GetMachineCertificate formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649759"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="8ec4b-106">IWMDRMSecurity:: GetMachineCertificate (método)</span><span class="sxs-lookup"><span data-stu-id="8ec4b-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="8ec4b-107">El método **GetMachineCertificate** recupera el certificado de equipo del subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec4b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ec4b-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="8ec4b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ec4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec4b-110">*dwCertificateType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ec4b-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4b-111">Tipo de certificado que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="8ec4b-112">Establezca en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="8ec4b-113">Value</span><span class="sxs-lookup"><span data-stu-id="8ec4b-113">Value</span></span>                        | <span data-ttu-id="8ec4b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec4b-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec4b-115">Tipo de certificado de WMDRM \_ \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="8ec4b-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="8ec4b-116">El certificado se recuperará en el formato utilizado por los componentes heredados.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="8ec4b-117">Tipo de certificado de WMDRM \_ \_ \_ V2</span><span class="sxs-lookup"><span data-stu-id="8ec4b-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="8ec4b-118">El certificado se recuperará en el formato utilizado por los componentes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8ec4b-119">*rgbVersion \[ 4 \]* \[\]</span><span class="sxs-lookup"><span data-stu-id="8ec4b-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4b-120">Matriz de cuatro bytes que especifica la versión del subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="8ec4b-121">*ppbCertificate* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ec4b-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4b-122">Dirección de una variable que recibe un puntero a los datos del certificado.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="8ec4b-123">Establezca en **null** para que el método proporcione el tamaño de búfer necesario para almacenar el certificado en *pcbCertificate*.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="8ec4b-124">*pcbCertificate* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ec4b-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4b-125">Tamaño del certificado en bytes.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="8ec4b-126">Si *ppbCertificate* es **null**, este valor se establecerá en el tamaño del certificado.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="8ec4b-127">Si *ppbCertificate* no es **null**, este valor debe establecerse en el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec4b-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec4b-128">Return value</span></span>

<span data-ttu-id="8ec4b-129">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ec4b-130">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ec4b-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec4b-131">Return code</span></span>                                                                          | <span data-ttu-id="8ec4b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec4b-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8ec4b-133"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4b-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8ec4b-134">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ec4b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec4b-135">Requirements</span></span>



| <span data-ttu-id="8ec4b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec4b-136">Requirement</span></span> | <span data-ttu-id="8ec4b-137">Value</span><span class="sxs-lookup"><span data-stu-id="8ec4b-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec4b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec4b-138">Header</span></span><br/>  | <dl> <span data-ttu-id="8ec4b-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4b-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ec4b-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ec4b-140">Library</span></span><br/> | <dl> <span data-ttu-id="8ec4b-141"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4b-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec4b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec4b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec4b-143">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="8ec4b-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





