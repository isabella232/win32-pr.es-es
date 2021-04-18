---
title: Método IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: El método MonitorLicenseAcquisition inicia la supervisión de un proceso de adquisición de licencias.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Método MonitorLicenseAcquisition formato de Windows Media
- Método MonitorLicenseAcquisition formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718604"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="3aa99-106">IWMDRMLicenseManagement:: MonitorLicenseAcquisition (método)</span><span class="sxs-lookup"><span data-stu-id="3aa99-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="3aa99-107">El método **MonitorLicenseAcquisition** inicia la supervisión de un proceso de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="3aa99-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa99-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aa99-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="3aa99-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3aa99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa99-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3aa99-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa99-111">IDENTIFICADOR de clave (KID) de la licencia adquirida.</span><span class="sxs-lookup"><span data-stu-id="3aa99-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="3aa99-112">*bstrHeader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3aa99-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa99-113">Encabezado de contenido usado en la llamada al método [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa99-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3aa99-114">*bstrActions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3aa99-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa99-115">Cadena que contiene las acciones solicitadas en la llamada al método **AcquireLicense** .</span><span class="sxs-lookup"><span data-stu-id="3aa99-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="3aa99-116">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3aa99-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa99-117">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3aa99-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="3aa99-118">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa99-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa99-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3aa99-119">Return value</span></span>

<span data-ttu-id="3aa99-120">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3aa99-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3aa99-121">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3aa99-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3aa99-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3aa99-122">Return code</span></span>                                                                          | <span data-ttu-id="3aa99-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3aa99-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3aa99-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa99-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3aa99-125">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3aa99-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3aa99-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3aa99-126">Remarks</span></span>

<span data-ttu-id="3aa99-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3aa99-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa99-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa99-128">Requirements</span></span>



| <span data-ttu-id="3aa99-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa99-129">Requirement</span></span> | <span data-ttu-id="3aa99-130">Value</span><span class="sxs-lookup"><span data-stu-id="3aa99-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa99-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3aa99-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa99-132"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa99-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3aa99-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3aa99-133">Library</span></span><br/> | <dl> <span data-ttu-id="3aa99-134"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aa99-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa99-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aa99-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa99-136">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="3aa99-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





