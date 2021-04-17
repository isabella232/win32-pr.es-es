---
title: Método IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: El método CreateLicenseEnumeration crea un objeto de enumerador de licencia con el que puede obtener información sobre las licencias en el almacén de licencias local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Método CreateLicenseEnumeration formato de Windows Media
- Método CreateLicenseEnumeration formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718641"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="f7c31-106">IWMDRMLicenseManagement:: CreateLicenseEnumeration (método)</span><span class="sxs-lookup"><span data-stu-id="f7c31-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="f7c31-107">El método **CreateLicenseEnumeration** crea un objeto de enumerador de licencia con el que puede obtener información sobre las licencias en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="f7c31-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c31-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7c31-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="f7c31-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7c31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7c31-110">*pLicenseFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7c31-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7c31-111">Puntero a una estructura de [**\_ \_ filtro de licencias de WMDRM**](wmdrm-license-filter.md) que contiene los parámetros de filtrado para la lista de licencias en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="f7c31-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="f7c31-112">*pEnumerator* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f7c31-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7c31-113">Puntero que recibe la dirección de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) del objeto enumerador de licencia recién creado.</span><span class="sxs-lookup"><span data-stu-id="f7c31-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7c31-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7c31-114">Return value</span></span>

<span data-ttu-id="f7c31-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f7c31-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f7c31-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f7c31-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f7c31-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f7c31-117">Return code</span></span>                                                                                                | <span data-ttu-id="f7c31-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7c31-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f7c31-119"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="f7c31-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="f7c31-120">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="f7c31-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="f7c31-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f7c31-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="f7c31-122">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f7c31-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f7c31-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7c31-123">Remarks</span></span>

<span data-ttu-id="f7c31-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f7c31-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c31-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7c31-125">Requirements</span></span>



| <span data-ttu-id="f7c31-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7c31-126">Requirement</span></span> | <span data-ttu-id="f7c31-127">Value</span><span class="sxs-lookup"><span data-stu-id="f7c31-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c31-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7c31-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f7c31-129"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7c31-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7c31-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7c31-130">Library</span></span><br/> | <dl> <span data-ttu-id="f7c31-131"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7c31-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7c31-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7c31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c31-133">**Enumerar licencias en el almacén de licencias local**</span><span class="sxs-lookup"><span data-stu-id="f7c31-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="f7c31-134">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="f7c31-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





