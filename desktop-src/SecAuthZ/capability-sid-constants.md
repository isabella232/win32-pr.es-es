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
# <a name="capability-sid-constants"></a>Constantes de SID de capacidad

Las constantes de SID de capacidad definen para las capacidades conocidas de las aplicaciones mediante la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**cliente de la funcionalidad de seguridad de \_ \_ Internet \_**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde un equipo cliente.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**funcionalidad de seguridad \_ \_ servidor de cliente de Internet \_ \_**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde los equipos cliente y servidor.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**funcionalidad de seguridad \_ \_ servidor de \_ cliente de red privada \_ \_**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde una red privada.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_biblioteca de \_ imágenes de capacidades de seguridad \_**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de imágenes.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_biblioteca de \_ vídeos de funcionalidades de seguridad \_**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de vídeos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_biblioteca de \_ música de funcionalidad de seguridad \_**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de música.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_biblioteca de \_ documentos de capacidad de seguridad \_**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de documentación.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_funcionalidad de \_ seguridad \_ autenticación empresarial**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Una cuenta tiene acceso a las credenciales predeterminadas de Windows.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_certificados de \_ usuario compartidos de capacidad de \_ seguridad \_**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Una cuenta tiene acceso a los certificados de usuario compartidos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ almacenamiento extraíble de la capacidad de seguridad \_**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Una cuenta tiene acceso al almacenamiento extraíble.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Al construir un SID de capacidad, debe incluir la entidad de paquete, la \_ \_ \_ entidad {0,0,0,0,0,15} de paquete de la aplicación de seguridad, en la llamada a la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) . Además, necesita el RID base y el recuento de RID para las funcionalidades integradas, \_ RID base de la funcionalidad de seguridad \_ \_ (0x00000003L) y el \_ recuento de RID de la capacidad integrada de seguridad \_ \_ \_ (2L).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

