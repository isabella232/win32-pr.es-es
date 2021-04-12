---
title: Método IBackgroundCopyFile2 SetRemoteName (Deliveryoptimization. h)
description: Cambia el nombre remoto a una nueva dirección URL en un trabajo de descarga.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Método SetRemoteName
- Método SetRemoteName, interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, método SetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490258"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="b7e1b-106">IBackgroundCopyFile2:: SetRemoteName (método)</span><span class="sxs-lookup"><span data-stu-id="b7e1b-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="b7e1b-107">Cambia el nombre remoto a una nueva dirección URL en un trabajo de descarga.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e1b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7e1b-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="b7e1b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7e1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e1b-110">*RemoteName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7e1b-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e1b-111">Cadena terminada en null que contiene el nombre del archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="b7e1b-112">Para obtener información sobre cómo especificar el nombre remoto, vea el miembro **RemoteName** .</span><span class="sxs-lookup"><span data-stu-id="b7e1b-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e1b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7e1b-113">Return value</span></span>

<span data-ttu-id="b7e1b-114">Este método devuelve los siguientes valores devueltos, así como otros.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="b7e1b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b7e1b-115">Return code</span></span>                                                                                  | <span data-ttu-id="b7e1b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7e1b-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7e1b-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="b7e1b-118">Correcto</span><span class="sxs-lookup"><span data-stu-id="b7e1b-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="b7e1b-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b7e1b-120">El nuevo nombre remoto es una dirección URL no válida o la nueva dirección URL es demasiado larga (la dirección URL no puede superar los 2.200 caracteres).</span><span class="sxs-lookup"><span data-stu-id="b7e1b-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7e1b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7e1b-121">Remarks</span></span>

<span data-ttu-id="b7e1b-122">Normalmente, se llama a este método si desea cambiar la dirección URL que se usa para transferir el archivo o si desea cambiar el nombre de archivo o la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="b7e1b-123">Este método no se serializa cuando devuelve.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="b7e1b-124">Para serializar el cambio, [**suspenda**](ibackgroundcopyjob-suspend.md) el trabajo, llame a este método (si va a cambiar varios archivos del trabajo, use un bucle) y [**reanude**](ibackgroundcopyjob-resume.md) el trabajo.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="b7e1b-125">Al llamar al método **IBackgroundCopyJob:: resume** se serializa el cambio.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="b7e1b-126">Si la marca de tiempo o el tamaño de archivo del nuevo nombre remoto es diferente del nombre remoto anterior o el nuevo servidor no admite el reinicio del punto de comprobación (para los nombres HTTP remotos), reinicia la descarga.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="b7e1b-127">De lo contrario, la transferencia se reanudará desde la misma posición en el nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="b7e1b-128">No reinicia los archivos ya transferidos.</span><span class="sxs-lookup"><span data-stu-id="b7e1b-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e1b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7e1b-129">Requirements</span></span>



| <span data-ttu-id="b7e1b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e1b-130">Requirement</span></span> | <span data-ttu-id="b7e1b-131">Value</span><span class="sxs-lookup"><span data-stu-id="b7e1b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e1b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7e1b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e1b-133">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7e1b-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7e1b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7e1b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e1b-135">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="b7e1b-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b7e1b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7e1b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e1b-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7e1b-138">IDL</span><span class="sxs-lookup"><span data-stu-id="b7e1b-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7e1b-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7e1b-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7e1b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7e1b-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b7e1b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7e1b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e1b-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1b-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b7e1b-144">IID</span><span class="sxs-lookup"><span data-stu-id="b7e1b-144">IID</span></span><br/>                      | <span data-ttu-id="b7e1b-145">IID_IBackgroundCopyFile2 se define como 83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="b7e1b-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b7e1b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7e1b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e1b-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="b7e1b-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





