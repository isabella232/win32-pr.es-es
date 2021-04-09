---
title: Clase auxiliar extensible de la plataforma de filtrado de Windows
description: La plataforma de filtrado de Windows (WFP) incluye una clase auxiliar del marco de diagnóstico de redes (NDF), denominada clase auxiliar de plataforma de filtrado (FPHC).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858835c1a649602293ed042c13205ca982de9258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995335"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Clase auxiliar extensible de la plataforma de filtrado de Windows

La [plataforma de filtrado de Windows (WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) incluye una clase auxiliar del marco de diagnóstico de redes (NDF), denominada clase auxiliar de plataforma de filtrado (FPHC). FPHC puede ayudar a identificar las causas raíz de los problemas de conectividad causados por WFP. Los desarrolladores de Firewall de terceros pueden implementar sus propias clases auxiliares de NDF. La extensibilidad de FPHC permite invocar estas clases auxiliares de terceros durante el diagnóstico.

En este tema se da por supuesto que está familiarizado con la [API de WFP](/windows/desktop/FWP/windows-filtering-platform-start-page).

## <a name="why-extend-the-fphc"></a>¿Por qué extender el FPHC?

Todos los desarrolladores que escriben aplicaciones que llaman a la API de WFP deben escribir una clase auxiliar NDF que extienda FPHC.

FPHC puede identificar WFP como causa de un problema de conectividad. Si está disponible, FPHC también puede identificar el proveedor que creó el filtro que está bloqueando el tráfico de red. FPHC pasa esta información a NDF, que a su vez puede notificar al usuario que WFP está causando el problema de conectividad y proporcionar el nombre del proveedor que bloquea el tráfico.

Sin embargo, el FPHC no puede sugerir una acción correctiva para el usuario, ni puede proporcionar el motivo por el que el filtro está bloqueando el tráfico al usuario. Solo una extensión FPHC puede realizar esas tareas.

Considere una aplicación de Firewall de terceros que llama a la API de WFP. Si el Firewall de terceros implementa una extensión FPHC, se pueden implementar acciones personalizadas para controlar los problemas de conectividad identificados por NDF. Cuando NDF diagnostica que una aplicación se ha bloqueado por el Firewall de terceros, la extensión FPHC puede controlar el evento de bloqueo. Una manera de que la extensión FPHC pueda controlar un evento es presentar al usuario un mensaje para desbloquear un programa mediante el firewall y, a continuación, desbloquear el programa tras la confirmación del usuario. Como alternativa, la extensión FPHC podría controlar un evento mediante la notificación al usuario de la razón por la que se bloqueó la aplicación, por ejemplo, si se bloqueó una aplicación porque el Firewall consideró malware.

## <a name="about-wfp-diagnostics"></a>Acerca del diagnóstico de WFP

Cuando se invoca NDF para diagnosticar un problema de red, se Contacta con las clases auxiliares para determinar la causa del problema. Si una clase auxiliar de nivel superior determina que un error de red puede estar causado por WFP, genera una hipótesis para FPHC basándose en la información disponible. NDF pasa esta hipótesis, en forma de varios atributos de evento, a FPHC. Estos atributos se describen en detalle en la sección [atributos de evento FPHC](#windows-filtering-platform-extensible-helper-class) a continuación.

Un problema de red puede describirse como un problema de conectividad que afecte a un intento de conexión determinado. Por ejemplo, puede que el usuario haya bloqueado accidentalmente una aplicación haciendo clic en **no permitir**. A continuación, el Firewall bloqueará la aplicación para que no se enlace a ningún puerto. El usuario, que no sabe por qué se bloquea la aplicación, puede intentar diagnosticar el problema a través de un punto de entrada ofrecido por la aplicación. FPHC examinará los registros y, si encuentra una coincidencia, recuperará el identificador de filtro y el ID. de proveedor de ese filtro en particular. En este punto, FPHC sabe quién es el propietario de ese filtro y se encargará del proceso de diagnóstico a la clase auxiliar adecuada para realizar un diagnóstico más exhaustivo.

El evento más reciente de los registros de eventos de WFP para que coincida con los atributos se selecciona como relacionado con el problema de la red. Si no se encuentra ningún evento coincidente y la hora en que se produjo el evento se trata en el registro de WFP, FPHC indica a NDF que es correcto. Si no se encuentra ningún evento coincidente y los registros de WFP no incluyen la hora en que se produjo el evento, FPHC devuelve un estado indeterminado a NDF.

Si se encuentra un evento coincidente, FPHC usa el identificador de proveedor del filtro que hizo que el evento identificara al proveedor de la regla de seguridad que bloqueó la conectividad. A continuación, FPHC comprueba si existe una extensión de clase auxiliar para ese proveedor. Si se encuentra uno, FPHC genera una hipótesis para ese proveedor y, a continuación, NDF invoca la extensión. La extensión debe devolver al usuario información útil de diagnóstico y reparación.

## <a name="helper-class-registration"></a>Registro de clases auxiliares

Se debe registrar una extensión FPHC como se describe en [registrar las extensiones de clase auxiliares de NDF](registering-ndf-helper-class-extensions.md). Los desarrolladores que implementan una clase auxiliar deben registrar sus extensiones para asegurarse de que NDF llama a la extensión cuando sea necesario. El *atributo coincidente que* se describe a continuación debe almacenarse en el registro, en **HKLM \\ System \\ CurrentControlSet \\ control \\ NetDiagFx** \\ *NombreProveedor* \\ **HostDLLs** \\ *helper Class dll* \\ **HelperClasses** \\ *nombre de clase auxiliar* \\ **MatchAttributes**.

En la tabla siguiente se muestra el atributo coincidente que se usa para identificar la hipótesis que se va a usar en los diagnósticos en el registro de eventos de WFP. 

| Nombre       | Tipo    | Descripción                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | Registro \_ SZ | GUID de la extensión FPHC. Este valor debe ser el mismo que el GUID del proveedor de WFP. <br/> Esta cadena distingue entre mayúsculas y minúsculas. Debe almacenarse en el registro en mayúsculas con llaves y guiones envolventes. Por ejemplo, {C200E360-38C5-11CE-AE62-08002B2B79EF} es un ProviderID válido.<br/> |



 

Cuando el ID. de registro de un filtro de bloqueo coincide con el de una clase auxiliar registrada, FPHC informa a NDF para invocar esa clase auxiliar, con lo que se amplía la capacidad de diagnóstico de FPHC.

## <a name="fphc-event-attributes"></a>Atributos de evento FPHC

En la tabla siguiente se enumeran los atributos de evento asociados a cada evento coincidente. Cada atributo de evento se almacena en una estructura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . NDF pasa estos atributos a FPHC cuando se encuentra un evento coincidente. A su vez, se pueden pasar a extensiones de FPHC.



| Atributo     | [**Atributo \_ de**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) Valor de tipo | Descripción                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de proveedor | EN \_ GUID                                        | GUID del proveedor asociado al filtro.                                                                                      |
| Timestamp     | en \_ cadena de octeto \_                               | Búfer de tipo FILETIME que especifica la hora a la que se produjo el evento. Esta marca de tiempo se puede usar para identificar de forma única un evento. |
| ipProtocol    | EN \_ UINT32                                      | Protocolo de capa de transporte, en formato UINT8.                                                                                            |
| LocalAddr     | EN \_ SOCKADDR                                    | La dirección IP local y el puerto, almacenados en una estructura [**Diag \_ SOCKADDR**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                             |
| RemoteAddr    | EN \_ SOCKADDR                                    | La dirección IP remota y el puerto, almacenados en una estructura [**Diag \_ SOCKADDR**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                            |
| userId        | en \_ cadena de octeto \_                               | Búfer de tipo SID que representa el UserID. Si userId es de longitud 0, el SID no está disponible.                                        |
| appId         | EN \_ cadena                                      | Búfer que almacena el identificador de la aplicación recuperado. Si appId tiene un valor de L "", el identificador de la aplicación no está disponible.        |



 

## <a name="handling-fphc-events"></a>Controlar eventos FPHC

Antes de sugerir información de diagnóstico y reparación para el usuario, una extensión FPHC debe recopilar más datos de los proporcionados por las notificaciones de FPHC. Estos datos se pueden adquirir de las [funciones de administración de eventos de WFP](/windows/desktop/FWP/fwp-mgmt-functions). Estas funciones se muestran en el ejemplo de [visualización de eventos de red](/windows/desktop/FWP/displaying-net-events) .

En el SDK se incluye un ejemplo de administración de eventos más detallado. El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WFP \\ DiagEvents. El SDK de Windows Vista está disponible en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

## <a name="built-in-fphc-diagnostics"></a>Diagnósticos integrados de FPHC

En ausencia de una extensión FPHC, FPHC puede diagnosticar los escenarios que se enumeran a continuación. La mayoría de los errores de conectividad diagnosticados por FPHC se producen porque los firewalls bloquean el tráfico. Los escenarios de IPsec son menos comunes.

En la tabla siguiente se muestran algunos escenarios que producen errores de conectividad que se pueden diagnosticar mediante FPHC, junto con la descripción y la información de reparación pasada a NDF.



| Escenario                   | Descripción de mantenimiento bajo                                                                                                               | Información de reparación                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Eliminación de Firewall              | La configuración del firewall en este equipo está bloqueando la conexión.                                                                  | Compruebe la configuración del firewall.       |
| Error de modo principal          | No se puede conectar debido a que una directiva de seguridad IPsec no coincide.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error de modo rápido         | No se puede conectar debido a que una directiva de seguridad IPsec no coincide.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error de modo de usuario          | No se puede conectar debido a que una directiva de seguridad IPsec no coincide.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error de credencial         | No se puede conectar porque la entidad de certificación raíz (CA) de este equipo no coincide con la CA raíz del equipo remoto. | Actualice el certificado raíz de confianza. |
| Certificado expirado        | Expiró el certificado usado para la autenticación IPsec.                                                                           | Solicitar un certificado.               |
| Otros errores de certificado | No se encontró un certificado válido para la autenticación IPsec.                                                                          | Solicitar un certificado.               |
| Error de Kerberos           | El equipo no forma parte de este dominio.                                                                                             | Unir este equipo a un dominio.      |
| Clave previamente compartida              | Restablezca las claves previamente compartidas.                                                                                                            | Restablezca las claves previamente compartidas.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Plataforma de filtrado de Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Diseñar extensiones de clase auxiliar NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registro de extensiones de clase auxiliar NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Ejemplos de la clase auxiliar NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

