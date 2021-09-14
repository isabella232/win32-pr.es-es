---
description: Defina para aplicaciones funcionalidades conocidas mediante la función AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes sid de funcionalidad (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168966"
---
# <a name="capability-sid-constants"></a>Constantes de SID de funcionalidad

Las constantes de SID de funcionalidad definen para las aplicaciones funcionalidades conocidas mediante la [**función AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**FUNCIONALIDAD \_ DE SEGURIDAD CLIENTE DE \_ INTERNET \_**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde un equipo cliente.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**FUNCIONALIDAD \_ DE SEGURIDAD SERVIDOR CLIENTE \_ DE INTERNET \_ \_**
</dt> <dd> <dl> <dt>

(0x000000002L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde los equipos cliente y servidor.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SERVIDOR \_ CLIENTE DE RED PRIVADA DE FUNCIONALIDAD DE \_ \_ \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde una red privada.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**BIBLIOTECA \_ DE IMÁGENES DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de imágenes.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**BIBLIOTECA DE \_ VÍDEOS DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000005L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de vídeos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**BIBLIOTECA \_ DE MÚSICA DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de música.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**BIBLIOTECA \_ DE DOCUMENTOS DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000007L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de documentación.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**FUNCIONALIDAD \_ DE SEGURIDAD \_ AUTENTICACIÓN \_ EMPRESARIAL**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Una cuenta tiene acceso a las credenciales Windows predeterminadas.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**CERTIFICADOS \_ DE USUARIO \_ COMPARTIDOS DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Una cuenta tiene acceso a los certificados de usuario compartidos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**ALMACENAMIENTO \_ EXTRAÍBLE DE LA FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Una cuenta tiene acceso al almacenamiento extraíble.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Al construir un SID de funcionalidad, debe incluir la entidad de paquete, SECURITY APP PACKAGE AUTHORITY , en la llamada a la \_ \_ función \_ {0,0,0,0,0,15} [**AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) Además, necesita el rid base y el recuento de RID para las funcionalidades integradas, SECURITY \_ CAPABILITY \_ BASE RID \_ (0x00000003L) y SECURITY \_ BUILTIN \_ CAPABILITY RID COUNT \_ \_ (2L).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



 

