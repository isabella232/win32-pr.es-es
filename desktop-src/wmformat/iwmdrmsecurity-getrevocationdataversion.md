---
title: Método IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: El método GetRevocationDataVersion recupera el número de versión de una lista de revocación de certificados en el almacén local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Método GetRevocationDataVersion formato de Windows Media
- Método GetRevocationDataVersion formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670568"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="90b9e-106">IWMDRMSecurity:: GetRevocationDataVersion (método)</span><span class="sxs-lookup"><span data-stu-id="90b9e-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="90b9e-107">El método **GetRevocationDataVersion** recupera el número de versión de una lista de revocación de certificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="90b9e-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b9e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90b9e-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="90b9e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90b9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b9e-110">*f \_ guidRevocationType* \[\]</span><span class="sxs-lookup"><span data-stu-id="90b9e-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90b9e-111">GUID que especifica el tipo de lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="90b9e-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="90b9e-112">Establezca en una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="90b9e-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="90b9e-113">Constante GUID</span><span class="sxs-lookup"><span data-stu-id="90b9e-113">GUID constant</span></span>                 | <span data-ttu-id="90b9e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b9e-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="90b9e-115">\_aplicación REVOCATIONTYPE de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="90b9e-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="90b9e-116">Especifica la lista de revocación de certificados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90b9e-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="90b9e-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="90b9e-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="90b9e-118">Especifica la lista de revocación de certificados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90b9e-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="90b9e-119">\_CARDEA REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="90b9e-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="90b9e-120">Especifica la lista de revocación de certificados de DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="90b9e-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="90b9e-121">*f \_ pdwCRLVersion* \[\]</span><span class="sxs-lookup"><span data-stu-id="90b9e-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90b9e-122">Variable que recibe el número de versión.</span><span class="sxs-lookup"><span data-stu-id="90b9e-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b9e-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90b9e-123">Return value</span></span>

<span data-ttu-id="90b9e-124">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="90b9e-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="90b9e-125">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="90b9e-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="90b9e-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="90b9e-126">Return code</span></span>                                                                          | <span data-ttu-id="90b9e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b9e-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="90b9e-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="90b9e-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="90b9e-129">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="90b9e-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="90b9e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90b9e-130">Requirements</span></span>



| <span data-ttu-id="90b9e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="90b9e-131">Requirement</span></span> | <span data-ttu-id="90b9e-132">Value</span><span class="sxs-lookup"><span data-stu-id="90b9e-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90b9e-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90b9e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="90b9e-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="90b9e-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="90b9e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90b9e-135">Library</span></span><br/> | <dl> <span data-ttu-id="90b9e-136"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90b9e-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b9e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="90b9e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b9e-138">**Revocación y renovación de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="90b9e-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="90b9e-139">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="90b9e-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="90b9e-140">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="90b9e-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="90b9e-141">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="90b9e-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





