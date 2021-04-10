---
description: Defina para las funcionalidades conocidas de las aplicaciones mediante la función AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes de SID de funcionalidad (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279635"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="79e92-103">Constantes de SID de capacidad</span><span class="sxs-lookup"><span data-stu-id="79e92-103">Capability SID Constants</span></span>

<span data-ttu-id="79e92-104">Las constantes de SID de capacidad definen para las capacidades conocidas de las aplicaciones mediante la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="79e92-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="79e92-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**cliente de la funcionalidad de seguridad de \_ \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-106">(0x00000001L)</span><span class="sxs-lookup"><span data-stu-id="79e92-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-107">Una cuenta tiene acceso a Internet desde un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="79e92-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**funcionalidad de seguridad \_ \_ servidor de cliente de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-109">(0x00000002L)</span><span class="sxs-lookup"><span data-stu-id="79e92-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-110">Una cuenta tiene acceso a Internet desde los equipos cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="79e92-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**funcionalidad de seguridad \_ \_ servidor de \_ cliente de red privada \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-112">(0x00000003L)</span><span class="sxs-lookup"><span data-stu-id="79e92-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-113">Una cuenta tiene acceso a Internet desde una red privada.</span><span class="sxs-lookup"><span data-stu-id="79e92-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_biblioteca de \_ imágenes de capacidades de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-115">(0x00000004L)</span><span class="sxs-lookup"><span data-stu-id="79e92-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-116">Una cuenta tiene acceso a la biblioteca de imágenes.</span><span class="sxs-lookup"><span data-stu-id="79e92-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_biblioteca de \_ vídeos de funcionalidades de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-118">(0x00000005L)</span><span class="sxs-lookup"><span data-stu-id="79e92-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-119">Una cuenta tiene acceso a la biblioteca de vídeos.</span><span class="sxs-lookup"><span data-stu-id="79e92-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_biblioteca de \_ música de funcionalidad de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-121">(0x00000006L)</span><span class="sxs-lookup"><span data-stu-id="79e92-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-122">Una cuenta tiene acceso a la biblioteca de música.</span><span class="sxs-lookup"><span data-stu-id="79e92-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_biblioteca de \_ documentos de capacidad de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-124">(0x00000007L)</span><span class="sxs-lookup"><span data-stu-id="79e92-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-125">Una cuenta tiene acceso a la biblioteca de documentación.</span><span class="sxs-lookup"><span data-stu-id="79e92-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_funcionalidad de \_ seguridad \_ autenticación empresarial**</span><span class="sxs-lookup"><span data-stu-id="79e92-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-127">(0x00000008L)</span><span class="sxs-lookup"><span data-stu-id="79e92-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-128">Una cuenta tiene acceso a las credenciales predeterminadas de Windows.</span><span class="sxs-lookup"><span data-stu-id="79e92-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_certificados de \_ usuario compartidos de capacidad de \_ seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-130">(0x00000009L)</span><span class="sxs-lookup"><span data-stu-id="79e92-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-131">Una cuenta tiene acceso a los certificados de usuario compartidos.</span><span class="sxs-lookup"><span data-stu-id="79e92-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79e92-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ almacenamiento extraíble de la capacidad de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="79e92-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e92-133">(0x0000000AL)</span><span class="sxs-lookup"><span data-stu-id="79e92-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="79e92-134">Una cuenta tiene acceso al almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="79e92-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79e92-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79e92-135">Remarks</span></span>

<span data-ttu-id="79e92-136">Al construir un SID de capacidad, debe incluir la entidad de paquete, la \_ \_ \_ entidad {0,0,0,0,0,15} de paquete de la aplicación de seguridad, en la llamada a la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="79e92-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="79e92-137">Además, necesita el RID base y el recuento de RID para las funcionalidades integradas, \_ RID base de la funcionalidad de seguridad \_ \_ (0x00000003L) y el \_ recuento de RID de la capacidad integrada de seguridad \_ \_ \_ (2L).</span><span class="sxs-lookup"><span data-stu-id="79e92-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e92-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e92-138">Requirements</span></span>



| <span data-ttu-id="79e92-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e92-139">Requirement</span></span> | <span data-ttu-id="79e92-140">Value</span><span class="sxs-lookup"><span data-stu-id="79e92-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79e92-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79e92-141">Minimum supported client</span></span><br/> | <span data-ttu-id="79e92-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="79e92-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79e92-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79e92-143">Minimum supported server</span></span><br/> | <span data-ttu-id="79e92-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="79e92-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79e92-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79e92-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="79e92-146"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e92-146"><dt>Winnt.h</dt></span></span> </dl> |



 

