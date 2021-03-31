---
title: DCOMSCMRemoteCallFlags
description: Controla el comportamiento de las llamadas desde el administrador de control de servicios (DCOMSCM) DCOM local a un DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valor del registro DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078424"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Controla el comportamiento de las llamadas desde el administrador de control de servicios (DCOMSCM) DCOM local a un DCOMSCM remoto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value | Descripción                                       |
|-------|---------------------------------------------------|
| 0x1   | **activación de DCOMSCM \_ \_ usar \_ todo \_ AUTHNSERVICES**  |
| 0x2   | **activación de DCOMSCM no \_ \_ permitir \_ llamada no segura \_** |
| 0x4   | **DCOMSCM \_ Resolve \_ usar \_ todo \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ resolver no \_ permitir \_ llamada no segura \_**    |
| 0x10  | **DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES Description

Cuando el cliente emite una solicitud de activación que usa la configuración de seguridad predeterminada, el DCOMSCM local usa el servicio de autenticación Negotiate al hacer la llamada RPC de activación al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de activación que usa el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de activación mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funcionan los proveedores de seguridad, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.

Al establecer esta marca, se puede realizar el DCOMSCM local en Windows Vista o superior para que se comporte como sistemas anteriores a vista. No se recomienda establecer esta marca a menos que sea necesaria por motivos de compatibilidad.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>Activación de DCOMSCM no \_ \_ permitir \_ Descripción de llamada no segura \_

Si se establece la marca de **activación DCOMSCM no \_ \_ permitir \_ \_ llamada no segura** , el DCOMSCM local no realiza una llamada RPC de activación no segura. Para permitir que los clientes realicen solicitudes de activación con una configuración de seguridad no predeterminada, especifique la estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) al efectuar la solicitud de activación. En este caso, se omiten las marcas de activación **DCOMSCM \_ \_ use \_ All \_ AUTHNSERVICES** y **DCOMSCM \_ Activate \_ Disallow \_ insecure \_ Call** Flags.

No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red se autentiquen por completo.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ resolver \_ uso de \_ toda la descripción de \_ AUTHNSERVICES

Cuando el cliente no calcula las referencias de una referencia de objeto, el DCOMSCM local usa el servicio de autenticación Negotiate al hacer la llamada RPC de resolución de OXID al DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de resolución de OXID sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de resolución de OXID mediante el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de resolución OXID mediante Kerberos, NTLM u otros proveedores de seguridad configurados. Si no funcionan los proveedores de seguridad, el DCOMSCM local realiza la llamada RPC de resolución de OXID sin seguridad.

Al establecer esta marca, se puede realizar el DCOMSCM local en Windows Vista o superior para que se comporte como sistemas anteriores a vista. No se recomienda establecer esta marca a menos que sea necesaria por motivos de compatibilidad.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ Resolve \_ denegar la descripción de la \_ llamada no segura \_

Si está establecida la marca de **DCOMSCM \_ resolver \_ denegar \_ \_ llamada no segura** , el DCOMSCM local no realiza una llamada RPC de resolución de Oxid no segura. Además, el DCOMSCM local no hace que una llamada RPC de ping de recolección de elementos no utilizados no sea segura. No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red se autentiquen por completo.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ ping \_ usar \_ Mid \_ AUTHNSERVICE Descripción

El DCOMSCM local usa el servicio de autenticación Negotiate al hacer que la llamada RPC de ping de recolección de elementos no utilizados se realice en el DCOMSCM remoto. Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de ping de recolección de elementos no utilizados sin seguridad.

**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de ping de recolección de elementos no utilizados con el servicio de autenticación Negotiate, el DCOMSCM local hace que la llamada RPC ping de la recolección de elementos no utilizados use Kerberos, NTLM y otros proveedores de seguridad configurados. Si no funcionan los proveedores de seguridad, el DCOMSCM local hace que la llamada RPC del ping de recolección de elementos no utilizados no sea de seguridad.

Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a vista. No se recomienda establecer la marca **DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE** a menos que sea necesario por motivos de compatibilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación para conexiones remotas](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 