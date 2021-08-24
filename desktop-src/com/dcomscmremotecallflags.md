---
title: DCOMSCMRemoteCallFlags
description: Controla el comportamiento de las llamadas desde el Administrador de control de servicios DCOM (DCOMSCM) local a un DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valor del Registro COM de DCOMSCMRemoteCallFlags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d658b80d347e684aa42aebad936a863b9bca2138b3118508849a730e11878d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678835"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controla el comportamiento de las llamadas desde el Administrador de control de servicios DCOM (DCOMSCM) local a un DCOMSCM remoto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor | Descripción                                       |
|-------|---------------------------------------------------|
| 0x1   | **ACTIVACIÓN DE DCOMSCM \_ \_ USE TODOS LOS \_ \_ AUTHNSERVICES**  |
| 0x2   | **ACTIVACIÓN DE DCOMSCM \_ NO PERMITE LA LLAMADA NO \_ \_ \_ SEGURA** |
| 0x4   | **RESOLUCIÓN DE DCOMSCM \_ \_ USE ALL \_ \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL**    |
| 0x10  | **PING DE DCOMSCM \_ \_ USE MID \_ \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>Activación de DCOMSCM \_ \_ USE ALL \_ \_ AUTHNSERVICES Description

Cuando el cliente emite una solicitud de activación que usa la configuración de seguridad predeterminada, el DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC de activación al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de activación que usa el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de activación mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funcionan proveedores de seguridad, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a Vista. No se recomienda establecer esta marca a menos que sea necesario por motivos de compatibilidad.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL Description

Si se establece la marca **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** , el DCOMSCM local no realiza una llamada RPC de activación no segura. Para permitir que los clientes realicen solicitudes de activación con una configuración de seguridad no predeterminada, especifique la [**estructura COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) al realizar la solicitud de activación. En este caso, las marcas **DCOMSCM \_ ACTIVATION USE ALL \_ \_ \_ AUTHNSERVICES** y **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** se omiten.

No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red estén totalmente autenticados.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES Description

Cuando el cliente desmarca una referencia a un objeto, el DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC de resolución DE LOD al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de resolución DE HAD sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de resolución DE DESAN mediante el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de resolución DE DESancha mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funciona ningún proveedor de seguridad, el DCOMSCM local realiza la llamada RPC de resolución DEMENTED sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a Vista. No se recomienda establecer esta marca a menos que sea necesario por motivos de compatibilidad.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL Description

Si se establece la marca **DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL** , el DCOMSCM local no realiza una llamada RPC de resolución DE DESAprotebración NO segura. Además, el DCOMSCM local no realiza una llamada RPC ping a la recolección de elementos no utilizados no segura. No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red estén totalmente autenticados.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ PING \_ USE \_ MID \_ AUTHNSERVICE Description

El DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC ping de recolección de elementos no utilizados al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC ping de recolección de elementos no utilizados sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC ping de recolección de elementos no utilizados mediante el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC ping a la recolección de elementos no utilizados mediante Kerberos, NTLM y otros proveedores de seguridad configurados. Si no funcionan proveedores de seguridad, el DCOMSCM local realiza la llamada RPC ping a la recolección de elementos no utilizados sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a Vista. No se recomienda establecer la marca **DCOMSCM \_ PING USE MID \_ \_ \_ AUTHNSERVICE** a menos que sea necesario por motivos de compatibilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación para conexiones remotas](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 