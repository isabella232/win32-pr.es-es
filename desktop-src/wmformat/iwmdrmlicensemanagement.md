---
title: Interfaz IWMDRMLicenseManagement
description: La interfaz IWMDRMLicenseManagement proporciona métodos que realizan operaciones generales relacionadas con el almacén de licencias local. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMLicenseManagement como parámetro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Interfaz IWMDRMLicenseManagement formato de Windows Media
- Interfaz IWMDRMLicenseManagement formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358087"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="82d24-106">Interfaz IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="82d24-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="82d24-107">La interfaz **IWMDRMLicenseManagement** proporciona métodos que realizan operaciones generales relacionadas con el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="82d24-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="82d24-108">Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="82d24-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="82d24-109">Pase el **IID \_ IWMDRMLicenseManagement** como parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="82d24-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="82d24-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="82d24-110">Members</span></span>

<span data-ttu-id="82d24-111">La interfaz **IWMDRMLicenseManagement** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="82d24-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="82d24-112">**IWMDRMLicenseManagement** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="82d24-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="82d24-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="82d24-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82d24-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="82d24-114">Methods</span></span>

<span data-ttu-id="82d24-115">La interfaz **IWMDRMLicenseManagement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="82d24-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="82d24-116">Método</span><span class="sxs-lookup"><span data-stu-id="82d24-116">Method</span></span>                                                                                               | <span data-ttu-id="82d24-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="82d24-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82d24-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="82d24-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="82d24-119">Adquiere de forma asincrónica una licencia de una dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="82d24-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="82d24-120">**BackupLicenses**</span><span class="sxs-lookup"><span data-stu-id="82d24-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="82d24-121">Crea una copia de seguridad de las licencias en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="82d24-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="82d24-122">**CleanLicenseStore**</span><span class="sxs-lookup"><span data-stu-id="82d24-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="82d24-123">Quita las licencias marcadas del almacén de licencias y desfragmenta el almacén para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="82d24-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="82d24-124">**CreateLicenseEnumeration**</span><span class="sxs-lookup"><span data-stu-id="82d24-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="82d24-125">Crea un objeto de enumerador de licencia rellenado con información de licencia basada en valores de parámetro.</span><span class="sxs-lookup"><span data-stu-id="82d24-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="82d24-126">**CreateLicenseRevocationChallenge**</span><span class="sxs-lookup"><span data-stu-id="82d24-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="82d24-127">Genera un desafío de revocación de licencia.</span><span class="sxs-lookup"><span data-stu-id="82d24-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="82d24-128">**DeleteLicense**</span><span class="sxs-lookup"><span data-stu-id="82d24-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="82d24-129">Elimina una licencia del almacén de licencias local temporal.</span><span class="sxs-lookup"><span data-stu-id="82d24-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="82d24-130">**MonitorLicenseAcquisition**</span><span class="sxs-lookup"><span data-stu-id="82d24-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="82d24-131">Inicia la supervisión de un proceso de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="82d24-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="82d24-132">**ProcessLicenseDeletionMessage**</span><span class="sxs-lookup"><span data-stu-id="82d24-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="82d24-133">Elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.</span><span class="sxs-lookup"><span data-stu-id="82d24-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="82d24-134">**ProcessLicenseRevocationResponse**</span><span class="sxs-lookup"><span data-stu-id="82d24-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="82d24-135">Revoca las licencias del almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="82d24-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="82d24-136">**RestoreLicenses**</span><span class="sxs-lookup"><span data-stu-id="82d24-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="82d24-137">Restaura las licencias de las que se realizó previamente una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="82d24-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="82d24-138">**StoreLicense**</span><span class="sxs-lookup"><span data-stu-id="82d24-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="82d24-139">Agrega una licencia al almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="82d24-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="82d24-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="82d24-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d24-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="82d24-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="82d24-142">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="82d24-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





