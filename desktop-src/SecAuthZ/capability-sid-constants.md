---
description: Defina para aplicaciones funcionalidades conocidas mediante la función AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes sid de funcionalidad (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37a06c0bd0115c4f7d05753825477b5de4948d1ddb9576aea46933a63cbf409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783219"
---
# <a name="capability-sid-constants"></a>Constantes sid de funcionalidad

Las constantes sid de funcionalidad definen para las aplicaciones funcionalidades conocidas mediante la [**función AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**CLIENTE \_ DE INTERNET DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
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

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SERVIDOR CLIENTE DE RED PRIVADA DE FUNCIONALIDAD \_ \_ DE \_ \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000003L)
</dt> <dt>



Una cuenta tiene acceso a Internet desde una red privada.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**BIBLIOTECA \_ DE IMÁGENES DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000004L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de imágenes.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**BIBLIOTECA \_ DE VÍDEOS DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000005L)
</dt> <dt>



Una cuenta tiene acceso a la biblioteca de vídeos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**BIBLIOTECA \_ DE MÚSICA DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000006L)
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

(0x000000008L)
</dt> <dt>



Una cuenta tiene acceso al valor predeterminado Windows credenciales.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**CERTIFICADOS \_ DE USUARIO COMPARTIDOS DE FUNCIONALIDAD \_ DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x000000009L)
</dt> <dt>



Una cuenta tiene acceso a los certificados de usuario compartidos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**ALMACENAMIENTO \_ EXTRAÍBLE DE FUNCIONALIDAD DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Una cuenta tiene acceso al almacenamiento extraíble.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Al construir un SID de funcionalidad, debe incluir la entidad de paquete, SECURITY APP PACKAGE AUTHORITY , en la llamada a la \_ \_ función \_ {0,0,0,0,0,15} [**AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) Además, necesita el rid base y el recuento de RID para las funcionalidades integradas, SECURITY \_ CAPABILITY \_ BASE RID \_ (0x00000003L) y SECURITY \_ BUILTIN \_ CAPABILITY RID COUNT \_ \_ (2L).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



 

