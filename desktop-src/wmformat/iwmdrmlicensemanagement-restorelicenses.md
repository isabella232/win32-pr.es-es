---
title: Método IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: El método RestoreLicenses restaura las licencias de una copia de seguridad de licencias que se creó mediante una llamada al método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Método RestoreLicenses formato de Windows Media
- Método RestoreLicenses formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718751"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="d70eb-106">IWMDRMLicenseManagement:: RestoreLicenses (método)</span><span class="sxs-lookup"><span data-stu-id="d70eb-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="d70eb-107">El método **RestoreLicenses** restaura las licencias de una copia de seguridad de licencias que se creó mediante una llamada al método [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .</span><span class="sxs-lookup"><span data-stu-id="d70eb-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70eb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d70eb-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="d70eb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d70eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70eb-110">*bstrBackupDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d70eb-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d70eb-111">Ruta de acceso UNC de la ubicación desde la que se restaurarán las licencias.</span><span class="sxs-lookup"><span data-stu-id="d70eb-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="d70eb-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d70eb-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d70eb-113">Marcas que especifican las opciones de restauración que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="d70eb-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="d70eb-114">La única marca admitida actualmente es la restauración de WMDRM \_ \_ individual, que configura el método para realizar una individualización como parte de la restauración, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d70eb-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="d70eb-115">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d70eb-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d70eb-116">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d70eb-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="d70eb-117">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="d70eb-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70eb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d70eb-118">Return value</span></span>

<span data-ttu-id="d70eb-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d70eb-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d70eb-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d70eb-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d70eb-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d70eb-121">Return code</span></span>                                                                          | <span data-ttu-id="d70eb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d70eb-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d70eb-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d70eb-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d70eb-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d70eb-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d70eb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d70eb-125">Remarks</span></span>

<span data-ttu-id="d70eb-126">Este método se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d70eb-126">This method executes asynchronously.</span></span> <span data-ttu-id="d70eb-127">Vuelve inmediatamente después de llamarlo y, a continuación, genera una serie de eventos **MEWMDRMLicenseRestoreProgress** seguidos de un evento **MEWMDRMLicenseRestoreCompleted** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="d70eb-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="d70eb-128">El valor de cada uno de los eventos **MEWMDRMLicenseRestoreProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="d70eb-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="d70eb-129">Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="d70eb-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="d70eb-130">Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="d70eb-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="d70eb-131">La copia de seguridad puede estar en el equipo local o desde un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="d70eb-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70eb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d70eb-132">Requirements</span></span>



| <span data-ttu-id="d70eb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70eb-133">Requirement</span></span> | <span data-ttu-id="d70eb-134">Value</span><span class="sxs-lookup"><span data-stu-id="d70eb-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d70eb-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d70eb-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d70eb-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70eb-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d70eb-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d70eb-137">Library</span></span><br/> | <dl> <span data-ttu-id="d70eb-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d70eb-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70eb-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d70eb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70eb-140">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="d70eb-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





