---
title: Método IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: El método CheckCertForRevocation determina si se ha revocado un certificado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Método CheckCertForRevocation formato de Windows Media
- Método CheckCertForRevocation formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649578"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="fd180-106">IWMDRMSecurity:: CheckCertForRevocation (método)</span><span class="sxs-lookup"><span data-stu-id="fd180-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="fd180-107">El método **CheckCertForRevocation** determina si se ha revocado un certificado.</span><span class="sxs-lookup"><span data-stu-id="fd180-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd180-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd180-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="fd180-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd180-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd180-110">*rguidRevocationList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd180-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd180-111">GUID que identifica la lista de revocación que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fd180-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="fd180-112">Establezca en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd180-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="fd180-113">Constante GUID</span><span class="sxs-lookup"><span data-stu-id="fd180-113">GUID constant</span></span>                 | <span data-ttu-id="fd180-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd180-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd180-115">\_aplicación REVOCATIONTYPE de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="fd180-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="fd180-116">Especifica la lista de revocación de certificados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd180-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="fd180-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="fd180-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="fd180-118">Especifica la lista de revocación de certificados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd180-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="fd180-119">\_CARDEA REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="fd180-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="fd180-120">Especifica la lista de revocación de certificados de DRM de Microsoft Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="fd180-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fd180-121">*pbCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd180-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd180-122">Búfer que contiene el certificado que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="fd180-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="fd180-123">*cbCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd180-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd180-124">Tamaño del búfer *pbCert*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="fd180-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fd180-125">*fRevoked* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fd180-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd180-126">En la salida, indica si el certificado está presente en la lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="fd180-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd180-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd180-127">Return value</span></span>

<span data-ttu-id="fd180-128">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fd180-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd180-129">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="fd180-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd180-130">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fd180-130">Return code</span></span>                                                                          | <span data-ttu-id="fd180-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd180-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd180-132"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fd180-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd180-133">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="fd180-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fd180-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd180-134">Requirements</span></span>



| <span data-ttu-id="fd180-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd180-135">Requirement</span></span> | <span data-ttu-id="fd180-136">Value</span><span class="sxs-lookup"><span data-stu-id="fd180-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd180-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd180-137">Header</span></span><br/>  | <dl> <span data-ttu-id="fd180-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd180-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd180-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd180-139">Library</span></span><br/> | <dl> <span data-ttu-id="fd180-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd180-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd180-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd180-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd180-142">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="fd180-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





