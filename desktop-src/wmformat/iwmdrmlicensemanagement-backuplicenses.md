---
title: Método IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: El método BackupLicenses crea una copia de seguridad de las licencias en el almacén de licencias local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Método BackupLicenses formato de Windows Media
- Método BackupLicenses formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718749"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="371db-106">IWMDRMLicenseManagement:: BackupLicenses (método)</span><span class="sxs-lookup"><span data-stu-id="371db-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="371db-107">El método **BackupLicenses** crea una copia de seguridad de las licencias en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="371db-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="371db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="371db-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="371db-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="371db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="371db-110">*bstrBackupDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="371db-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="371db-111">Ruta de acceso UNC de la ubicación en la que se realizará la copia de seguridad de las licencias.</span><span class="sxs-lookup"><span data-stu-id="371db-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="371db-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="371db-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="371db-113">Marcas que especifican las opciones de copia de seguridad que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="371db-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="371db-114">La única marca admitida actualmente es \_ \_ sobrescribir la copia de seguridad de WMDRM, que configura el método para sobrescribir los archivos de copia de seguridad existentes en el directorio.</span><span class="sxs-lookup"><span data-stu-id="371db-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="371db-115">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="371db-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="371db-116">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="371db-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="371db-117">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="371db-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="371db-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="371db-118">Return value</span></span>

<span data-ttu-id="371db-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="371db-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="371db-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="371db-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="371db-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="371db-121">Return code</span></span>                                                                          | <span data-ttu-id="371db-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="371db-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="371db-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="371db-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="371db-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="371db-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="371db-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="371db-125">Remarks</span></span>

<span data-ttu-id="371db-126">Este método se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="371db-126">This method executes asynchronously.</span></span> <span data-ttu-id="371db-127">Vuelve inmediatamente después de llamarlo y, a continuación, genera una serie de eventos **MEWMDRMLicenseBackupProgress** seguidos de un evento **MEWMDRMLicenseBackupCompleted** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="371db-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="371db-128">El valor de cada uno de los eventos **MEWMDRMLicenseBackupProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="371db-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="371db-129">Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="371db-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="371db-130">Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="371db-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="371db-131">No se permite realizar copias de seguridad de todas las licencias.</span><span class="sxs-lookup"><span data-stu-id="371db-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="371db-132">Este método solo realiza una copia de seguridad de las licencias que lo permiten.</span><span class="sxs-lookup"><span data-stu-id="371db-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="371db-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="371db-133">Requirements</span></span>



| <span data-ttu-id="371db-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="371db-134">Requirement</span></span> | <span data-ttu-id="371db-135">Value</span><span class="sxs-lookup"><span data-stu-id="371db-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="371db-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="371db-136">Header</span></span><br/>  | <dl> <span data-ttu-id="371db-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="371db-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="371db-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="371db-138">Library</span></span><br/> | <dl> <span data-ttu-id="371db-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="371db-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="371db-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="371db-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371db-141">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="371db-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





