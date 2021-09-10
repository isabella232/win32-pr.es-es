---
title: DCOMSCMRemoteCallFlags
description: Controla el comportamiento de las llamadas desde el Administrador de control de servicios DCOM (DCOMSCM) local a un DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valor del Registro COM de DCOMSCMRemoteCallFlags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369659"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controla el comportamiento de las llamadas desde el Administrador de control de servicios DCOM (DCOMSCM) local a un DCOMSCM remoto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG DWORD.**



| Value | Descripción                                       |
|-------|---------------------------------------------------|
| 0x1   | **ACTIVACIÓN DE DCOMSCM \_ \_ USE TODOS LOS \_ \_ AUTHNSERVICES**  |
| 0x2   | **ACTIVACIÓN DE DCOMSCM \_ NO PERMITIR LLAMADA NO \_ \_ \_ SEGURA** |
| 0x4   | **RESOLUCIÓN DE DCOMSCM \_ \_ USE ALL \_ \_ AUTHNSERVICES (USAR TODOS LOS AUTHNSERVICES)**     |
| 0x8   | **DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL**    |
| 0x10  | **PING DE DCOMSCM \_ \_ USE MID \_ \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>ACTIVACIÓN DE DCOMSCM \_ USE LA descripción DE TODOS LOS \_ \_ \_ AUTHNSERVICES

Cuando el cliente emite una solicitud de activación que usa la configuración de seguridad predeterminada, el DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC de activación al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de activación que usa el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de activación mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funciona ningún proveedor de seguridad, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a Vista. No se recomienda establecer esta marca a menos que sea necesario por motivos de compatibilidad.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>Activación de DCOMSCM \_ NO PERMITIR descripción DE LLAMADA NO \_ \_ \_ SEGURA

Si la **marca DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL** está establecida, el DCOMSCM local no realiza una llamada RPC de activación no segura. Para permitir que los clientes realicen solicitudes de activación con una configuración de seguridad no predeterminada, especifique la [**estructura COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) al realizar la solicitud de activación. En este caso, se omiten las marcas DE LLAMADAS NO SEGURAS USE **\_ ALL \_ \_ \_ AUTHNSERVICES** y **DCOMSCM \_ ACTIVATION \_ DISALLOW \_ UNSECURE \_ CALL.**

No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red estén totalmente autenticados.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>RESOLUCIÓN DE DCOMSCM \_ \_ USE ALL \_ \_ AUTHNSERVICES Description

Cuando el cliente desmarshals una referencia de objeto, el DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC de resolución DEMENTED al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de resolución DE PXD sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de resolución de RPC de SAML que usa el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de resolución DE PXD mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funciona ningún proveedor de seguridad, el DCOMSCM local realiza la llamada RPC de resolución DEMENTED sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a Vista. No se recomienda establecer esta marca a menos que sea necesario por motivos de compatibilidad.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL Description

Si la **marca DCOMSCM \_ RESOLVE \_ DISALLOW \_ UNSECURE \_ CALL** está establecida, el DCOMSCM local no realiza una llamada RPC de resolución DEMENTED no segura. Además, el DCOMSCM local no realiza una llamada RPC ping a la recolección de elementos no utilizados no segura. No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red estén totalmente autenticados.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ PING \_ USE \_ MID \_ AUTHNSERVICE Description

El DCOMSCM local usa el servicio de autenticación Negotiate al realizar la llamada RPC ping de recolección de elementos no utilizados al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC ping de recolección de elementos no utilizados sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC ping de recolección de elementos no utilizados mediante el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC ping de recolección de elementos no utilizados mediante Kerberos, NTLM y otros proveedores de seguridad configurados. Si no funciona ningún proveedor de seguridad, el DCOMSCM local realiza la llamada RPC ping a la recolección de elementos no utilizados sin seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o versiones posteriores se comporte como sistemas anteriores a Vista. No se recomienda establecer la marca **DCOMSCM \_ PING USE MID \_ \_ \_ AUTHNSERVICE** a menos que sea necesario por motivos de compatibilidad.

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

 

 