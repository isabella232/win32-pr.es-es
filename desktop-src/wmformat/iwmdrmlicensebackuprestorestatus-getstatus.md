---
title: Método GetStatus de IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: El método GetStatus recupera información de estado detallada sobre una operación de copia de seguridad o restauración de una licencia.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Método GetStatus formato de Windows Media
- Método GetStatus formato de Windows Media, interfaz IWMDRMLicenseBackupRestoreStatus
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709170"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="8f12c-106">IWMDRMLicenseBackupRestoreStatus:: GetStatus (método)</span><span class="sxs-lookup"><span data-stu-id="8f12c-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="8f12c-107">El método **getStatus** recupera información de estado detallada sobre una operación de copia de seguridad o restauración de una licencia.</span><span class="sxs-lookup"><span data-stu-id="8f12c-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f12c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f12c-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8f12c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f12c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f12c-110">*pStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f12c-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f12c-111">Puntero a una estructura de [**Estado de restauración de copia de seguridad de WM \_ \_ \_**](wm-backup-restore-status.md) que recibe la información de estado.</span><span class="sxs-lookup"><span data-stu-id="8f12c-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f12c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f12c-112">Return value</span></span>

<span data-ttu-id="8f12c-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8f12c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8f12c-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8f12c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8f12c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8f12c-115">Return code</span></span>                                                                          | <span data-ttu-id="8f12c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f12c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8f12c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8f12c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8f12c-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8f12c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f12c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f12c-119">Remarks</span></span>

<span data-ttu-id="8f12c-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f12c-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f12c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f12c-121">Requirements</span></span>



| <span data-ttu-id="8f12c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f12c-122">Requirement</span></span> | <span data-ttu-id="8f12c-123">Value</span><span class="sxs-lookup"><span data-stu-id="8f12c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f12c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f12c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8f12c-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f12c-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f12c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f12c-126">Library</span></span><br/> | <dl> <span data-ttu-id="8f12c-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f12c-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f12c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f12c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f12c-129">**Interfaz IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="8f12c-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





