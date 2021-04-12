---
title: Interfaz IWMDRMLicenseBackupRestoreStatus
description: La interfaz IWMDRMLicenseBackupRestoreStatus proporciona un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias. Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359260"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="31a30-105">Interfaz IWMDRMLicenseBackupRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="31a30-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="31a30-106">La interfaz **IWMDRMLicenseBackupRestoreStatus** proporciona un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="31a30-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="31a30-107">Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="31a30-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="31a30-108">Se generan varios eventos **MEWMDRMLicenseBackupProgress** durante la copia de seguridad de la licencia, cada uno de los cuales tiene una instancia adjunta de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="31a30-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="31a30-109">Lo mismo se aplica a los eventos **MEWMDRMLicenseRestoreProgress** , que se generan durante la restauración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="31a30-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="31a30-110">Para recuperar un puntero a una instancia de la interfaz **IWMDRMLicenseBackupRestoreStatus** , primero debe llamar al método **IMFMediaEvent:: GetValue** del evento progress.</span><span class="sxs-lookup"><span data-stu-id="31a30-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="31a30-111">El valor que se recupera del evento es un puntero a la interfaz **IUnknown** del objeto que implementa la interfaz **IWMDRMLicenseBackupRestoreStatus** .</span><span class="sxs-lookup"><span data-stu-id="31a30-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="31a30-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="31a30-112">Members</span></span>

<span data-ttu-id="31a30-113">La interfaz **IWMDRMLicenseBackupRestoreStatus** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="31a30-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="31a30-114">**IWMDRMLicenseBackupRestoreStatus** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31a30-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="31a30-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="31a30-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="31a30-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="31a30-116">Methods</span></span>

<span data-ttu-id="31a30-117">La interfaz **IWMDRMLicenseBackupRestoreStatus** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="31a30-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="31a30-118">Método</span><span class="sxs-lookup"><span data-stu-id="31a30-118">Method</span></span>                                                          | <span data-ttu-id="31a30-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="31a30-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31a30-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="31a30-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="31a30-121">Recupera información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="31a30-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="31a30-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="31a30-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a30-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="31a30-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

