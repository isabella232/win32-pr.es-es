---
title: Interfaz IWMDRMSecurity
description: La interfaz IWMDRMSecurity administra una gran variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM). Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Interfaz IWMDRMSecurity formato de Windows Media
- Interfaz IWMDRMSecurity formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358178"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="4d68f-105">Interfaz IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="4d68f-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="4d68f-106">La interfaz **IWMDRMSecurity** administra una gran variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="4d68f-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="4d68f-107">Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="4d68f-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="4d68f-108">Pase el **IID \_ IWMDRMSecurity** como parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="4d68f-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="4d68f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d68f-109">Members</span></span>

<span data-ttu-id="4d68f-110">La interfaz **IWMDRMSecurity** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="4d68f-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="4d68f-111">**IWMDRMSecurity** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d68f-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="4d68f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d68f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4d68f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d68f-113">Methods</span></span>

<span data-ttu-id="4d68f-114">La interfaz **IWMDRMSecurity** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4d68f-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="4d68f-115">Método</span><span class="sxs-lookup"><span data-stu-id="4d68f-115">Method</span></span>                                                                                      | <span data-ttu-id="4d68f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d68f-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d68f-117">**CheckCertForRevocation**</span><span class="sxs-lookup"><span data-stu-id="4d68f-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="4d68f-118">Determina si se ha revocado un certificado.</span><span class="sxs-lookup"><span data-stu-id="4d68f-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="4d68f-119">**GetContentEnablersForRevocations**</span><span class="sxs-lookup"><span data-stu-id="4d68f-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="4d68f-120">Recupera interfaces del habilitador de contenido que habilita la renovación de componentes basándose en certificados revocados.</span><span class="sxs-lookup"><span data-stu-id="4d68f-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="4d68f-121">**GetContentEnablersFromHashes**</span><span class="sxs-lookup"><span data-stu-id="4d68f-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="4d68f-122">Recupera interfaces del habilitador de contenido que habilita la renovación de componentes basándose en certificados hash.</span><span class="sxs-lookup"><span data-stu-id="4d68f-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="4d68f-123">**GetMachineCertificate**</span><span class="sxs-lookup"><span data-stu-id="4d68f-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="4d68f-124">Recupera el certificado de equipo del subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="4d68f-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="4d68f-125">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="4d68f-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="4d68f-126">Recupera una lista de revocación de certificados del almacén local.</span><span class="sxs-lookup"><span data-stu-id="4d68f-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="4d68f-127">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="4d68f-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="4d68f-128">Recupera el número de versión de una lista de revocación de certificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="4d68f-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="4d68f-129">**GetSecurityVersion**</span><span class="sxs-lookup"><span data-stu-id="4d68f-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="4d68f-130">Recupera la versión del subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="4d68f-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="4d68f-131">**PerformSecurityUpdate**</span><span class="sxs-lookup"><span data-stu-id="4d68f-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="4d68f-132">Inicia una actualización de seguridad para el subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="4d68f-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="4d68f-133">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="4d68f-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="4d68f-134">Establece una lista de revocación de certificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="4d68f-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="4d68f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d68f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d68f-136">**Ejemplo de individualización de DRM**</span><span class="sxs-lookup"><span data-stu-id="4d68f-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="4d68f-137">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="4d68f-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4d68f-138">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="4d68f-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





