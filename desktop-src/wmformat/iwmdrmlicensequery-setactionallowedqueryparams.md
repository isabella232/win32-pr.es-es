---
title: Método IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: El método SetActionAllowedQueryParams establece la información específica del entorno para obtener resultados de consulta más precisos cuando se usa el método QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Método SetActionAllowedQueryParams formato de Windows Media
- Método SetActionAllowedQueryParams formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679146"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="36802-106">IWMDRMLicenseQuery:: SetActionAllowedQueryParams (método)</span><span class="sxs-lookup"><span data-stu-id="36802-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="36802-107">El método **SetActionAllowedQueryParams** establece la información específica del entorno para obtener resultados de consulta más precisos cuando se usa el método [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .</span><span class="sxs-lookup"><span data-stu-id="36802-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36802-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36802-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="36802-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36802-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36802-110">*fIsMF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36802-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36802-111">Especifica si el contenido se representará mediante los objetos del SDK de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="36802-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="36802-112">**False** indica la representación de los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="36802-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="36802-113">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="36802-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="36802-114">*dwAppSecLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36802-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36802-115">Nivel de seguridad de la aplicación que se consulta.</span><span class="sxs-lookup"><span data-stu-id="36802-115">Security level of the querying application.</span></span> <span data-ttu-id="36802-116">Este valor solo es importante si se van a utilizar los objetos del SDK de Windows Media Format, en cuyo caso *fIsMF* debe establecerse en **false**.</span><span class="sxs-lookup"><span data-stu-id="36802-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="36802-117">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="36802-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="36802-118">*fHasSerialNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36802-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36802-119">Especifica si el dispositivo de destino para una operación de copia tiene un número de serie.</span><span class="sxs-lookup"><span data-stu-id="36802-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="36802-120">Este parámetro es opcional y solo se aplica a las consultas de operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="36802-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="36802-121">*bstrDeviceCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36802-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36802-122">Certificado de dispositivo del dispositivo de destino al usar DRM de Windows Media para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="36802-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="36802-123">Este parámetro es opcional y solo se aplica a las consultas de operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="36802-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36802-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36802-124">Return value</span></span>

<span data-ttu-id="36802-125">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="36802-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="36802-126">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="36802-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="36802-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="36802-127">Return code</span></span>                                                                          | <span data-ttu-id="36802-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="36802-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="36802-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="36802-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="36802-130">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="36802-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36802-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36802-131">Remarks</span></span>

<span data-ttu-id="36802-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36802-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="36802-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36802-133">Requirements</span></span>



| <span data-ttu-id="36802-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36802-134">Requirement</span></span> | <span data-ttu-id="36802-135">Value</span><span class="sxs-lookup"><span data-stu-id="36802-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36802-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36802-136">Header</span></span><br/>  | <dl> <span data-ttu-id="36802-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="36802-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="36802-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36802-138">Library</span></span><br/> | <dl> <span data-ttu-id="36802-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36802-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36802-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="36802-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36802-141">**Interfaz IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="36802-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="36802-142">**Consulta para obtener información detallada sobre los derechos**</span><span class="sxs-lookup"><span data-stu-id="36802-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





