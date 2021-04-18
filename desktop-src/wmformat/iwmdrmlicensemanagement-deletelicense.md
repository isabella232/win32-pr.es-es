---
title: Método IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: El método DeleteLicense quita una licencia del almacén de licencias local temporal.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Método DeleteLicense formato de Windows Media
- Método DeleteLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718803"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="f0d8f-106">IWMDRMLicenseManagement::D método eleteLicense</span><span class="sxs-lookup"><span data-stu-id="f0d8f-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="f0d8f-107">El método **DeleteLicense** quita una licencia del almacén de licencias local temporal.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d8f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0d8f-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f0d8f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0d8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d8f-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d8f-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d8f-111">IDENTIFICADOR de clave (KID) de la licencia que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="f0d8f-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d8f-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d8f-113">Marcas de opciones de eliminación de licencias.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-113">License deletion option flags.</span></span> <span data-ttu-id="f0d8f-114">Establezca en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="f0d8f-115">Value</span><span class="sxs-lookup"><span data-stu-id="f0d8f-115">Value</span></span>                                    | <span data-ttu-id="f0d8f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0d8f-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d8f-117">la \_ licencia de eliminación de WMDRM \_ \_ inmediatamente</span><span class="sxs-lookup"><span data-stu-id="f0d8f-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="f0d8f-118">Especifica que la licencia se debe quitar del almacén de inmediato.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="f0d8f-119">\_ \_ \_ marca \_ de eliminación de licencia de WMDRM para \_ purgar</span><span class="sxs-lookup"><span data-stu-id="f0d8f-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="f0d8f-120">Especifica que la licencia debe marcarse para su eliminación, pero no debe quitarse del almacén hasta que se llame al método [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d8f-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d8f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0d8f-121">Return value</span></span>

<span data-ttu-id="f0d8f-122">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f0d8f-123">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f0d8f-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f0d8f-124">Return code</span></span>                                                                                            | <span data-ttu-id="f0d8f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0d8f-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0d8f-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8f-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f0d8f-127">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="f0d8f-128"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8f-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="f0d8f-129">La licencia especificada no existe en el almacén.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="f0d8f-130">O bien</span><span class="sxs-lookup"><span data-stu-id="f0d8f-130">- OR -</span></span><br/> <span data-ttu-id="f0d8f-131">No se encontró el almacén.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0d8f-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0d8f-132">Remarks</span></span>

<span data-ttu-id="f0d8f-133">Para eliminar licencias del almacén de licencias local permanente, debe usar la revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="f0d8f-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d8f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0d8f-134">Requirements</span></span>



| <span data-ttu-id="f0d8f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d8f-135">Requirement</span></span> | <span data-ttu-id="f0d8f-136">Value</span><span class="sxs-lookup"><span data-stu-id="f0d8f-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d8f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0d8f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f0d8f-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8f-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0d8f-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0d8f-139">Library</span></span><br/> | <dl> <span data-ttu-id="f0d8f-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8f-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d8f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0d8f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d8f-142">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="f0d8f-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





