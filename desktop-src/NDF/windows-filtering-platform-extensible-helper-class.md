---
title: Windows Clase auxiliar extensible de la plataforma de filtrado
description: La Windows filtering platform (WFP) incluye una clase auxiliar Marco de diagnóstico de redes (NDF), denominada clase auxiliar de plataforma de filtrado (FPHC).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858835c1a649602293ed042c13205ca982de9258
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476759"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows Clase auxiliar extensible de la plataforma de filtrado

La [Windows filtering platform (WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) incluye una clase auxiliar Marco de diagnóstico de redes (NDF), denominada clase auxiliar de plataforma de filtrado (FPHC). FPHC puede ayudar a identificar las causas principales de los problemas de conectividad causados por WFP. Los desarrolladores de firewall de terceros pueden implementar sus propias clases auxiliares de NDF. La extensibilidad FPHC permite invocar estas clases auxiliares de terceros durante el diagnóstico.

En este tema se da por supuesto que está familiarizado con la [API de WFP.](/windows/desktop/FWP/windows-filtering-platform-start-page)

## <a name="why-extend-the-fphc"></a>¿Por qué extender fphc?

Todos los desarrolladores que escriben aplicaciones que llaman a la API de WFP deben escribir una clase auxiliar de NDF que extienda FPHC.

FPHC puede identificar WFP como la causa de un problema de conectividad. Si está disponible, FPHC también puede identificar el proveedor que creó el filtro que está bloqueando el tráfico de red. FPHC pasa esta información a NDF, que a su vez puede notificar al usuario que WFP está causando el problema de conectividad y dar el nombre del proveedor que bloquea el tráfico.

Sin embargo, FPHC no puede sugerir una acción correctiva al usuario, ni puede proporcionar la razón por la que el filtro está bloqueando el tráfico al usuario. Solo una extensión FPHC puede realizar esas tareas.

Considere la posibilidad de usar una aplicación de firewall de terceros que llame a la API de WFP. Si el firewall de terceros implementa una extensión FPHC, se pueden implementar acciones personalizadas para controlar los problemas de conectividad identificados por NDF. Cuando NDF diagnostica que el firewall de terceros ha bloqueado una aplicación, la extensión FPHC puede controlar el evento de bloqueo. Una manera de que la extensión FPHC pueda controlar un evento es presentar al usuario una solicitud para desbloquear un programa mediante el firewall y, a continuación, desbloquear el programa tras la confirmación del usuario. Como alternativa, la extensión FPHC podría controlar un evento notificando al usuario el motivo por el que se bloqueó la aplicación, como que una aplicación se bloqueó porque el firewall lo consideró malware.

## <a name="about-wfp-diagnostics"></a>Acerca de los diagnósticos de WFP

Cuando se invoca NDF para diagnosticar un problema de red, se contacta con las clases auxiliares para determinar la causa del problema. Si una clase auxiliar de nivel superior determina que un error de red puede deberse a WFP, genera una hipótesis para FPHC basada en la información disponible. NDF pasa esta hipótesis, en forma de varios atributos de evento, a FPHC. Estos atributos se describen en detalle en la [sección Atributos de evento FPHC siguiente.](#windows-filtering-platform-extensible-helper-class)

Un problema de red se puede describir como un problema de conectividad que afecta a un intento de conexión determinado. Por ejemplo, es posible que el usuario haya bloqueado accidentalmente una aplicación haciendo clic involuntariamente en **No permitir**. A continuación, el firewall impedirá que la aplicación se enlace a cualquier puerto. El usuario, sin saber por qué se bloquea la aplicación, puede intentar diagnosticar el problema a través de un punto de entrada que ofrece la aplicación. FPHC consultará los registros y, si encuentra una coincidencia, recuperará el identificador de filtro y el identificador de proveedor de ese filtro concreto. En este momento, FPHC sabe quién es el propietario de ese filtro y pasará el proceso de diagnóstico a la clase auxiliar adecuada para un diagnóstico posterior.

El evento más reciente en los registros de eventos WFP para que coincidan con los atributos se selecciona como relevante para el problema de red. Si no se encuentran eventos que coincidan y la hora en que se produjo el evento se cubre en el registro de WFP, FPHC indica a NDF que está en buen estado. Si no se encuentra ningún evento que coincida y los registros de WFP no incluyen la hora en que se produjo el evento, FPHC devuelve un estado indeterminado a NDF.

Si se encuentra un evento de coincidencia, FPHC usa el identificador de proveedor del filtro que hizo que el evento identificara al proveedor de la regla de seguridad que bloqueaba la conectividad. A continuación, FPHC comprueba si existe una extensión de clase auxiliar para ese proveedor. Si se encuentra uno, FPHC genera una hipótesis para ese proveedor y, a continuación, NDF invoca la extensión. La extensión debe devolver información útil de diagnóstico y reparación al usuario.

## <a name="helper-class-registration"></a>Registro de clases auxiliares

Se debe registrar una extensión FPHC como se describe en Registro de extensiones de clase [auxiliar de NDF](registering-ndf-helper-class-extensions.md). Los desarrolladores que implementan una clase auxiliar deben registrar sus extensiones para asegurarse de que NDF llama a la extensión cuando sea necesario. El  atributo correspondiente que se describe a continuación debe almacenarse en el Registro en **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class DLL* \\ **HelperClasses** Helper \\ *Class* \\ **MatchAttributes**.

En la tabla siguiente se muestra el atributo de coincidencia utilizado para identificar la hipótesis que se usará en los diagnósticos en el registro de eventos WFP. 

| Nombre       | Tipo    | Descripción                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ SZ | GUID de la extensión FPHC. Este valor debe ser el mismo que el GUID del proveedor WFP. <br/> Esta cadena distingue mayúsculas de minúsculas. Debe almacenarse en el Registro en mayúsculas con llaves y guiones. Por ejemplo, {C200E360-38C5-11CE-AE62-08002B2B79EF} es un ProviderID válido.<br/> |



 

Cuando providerID de un filtro de bloqueo coincide con el de una clase auxiliar registrada, FPHC informa a NDF de que invoque esa clase auxiliar, ampliando así la funcionalidad de diagnóstico de FPHC.

## <a name="fphc-event-attributes"></a>Atributos de evento FPHC

En la tabla siguiente se enumeran los atributos de evento asociados a cada evento de coincidencia. Cada atributo de evento se almacena en una [**estructura HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) NDF pasa estos atributos a FPHC cuando se encuentra un evento de coincidencia. A su vez, se pueden pasar a las extensiones FPHC.



| Atributo     | [**ATTRIBUTE \_ VALOR DE**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) TIPO | Descripción                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID del proveedor | GUID \_ de AT                                        | GUID del proveedor asociado al filtro.                                                                                      |
| Timestamp     | AT \_ OCTET \_ STRING                               | Búfer de tipo FILETIME que especifica la hora a la que se produjo el evento. Esta marca de tiempo se puede usar para identificar de forma única un evento. |
| ipProtocol    | AT \_ UINT32                                      | Protocolo de capa de transporte, en formato UINT8.                                                                                            |
| LocalAddr     | AT \_ SOCKADDR                                    | La dirección IP local y el puerto, almacenados en una [**estructura \_ SOCKADDR de DIAG.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                             |
| RemoteAddr    | AT \_ SOCKADDR                                    | La dirección IP remota y el puerto, almacenados en una [**estructura \_ SOCKADDR de DIAG.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                            |
| userId        | AT \_ OCTET \_ STRING                               | Búfer de tipo SID que representa el userid. Si userId tiene una longitud de 0, el SID no está disponible.                                        |
| appId         | AT \_ STRING                                      | Búfer que almacena el identificador de aplicación recuperado. Si appId tiene un valor de L""", el identificador de aplicación no está disponible.        |



 

## <a name="handling-fphc-events"></a>Control de eventos FPHC

Antes de sugerir información de diagnóstico y reparación al usuario, una extensión FPHC debe recopilar más datos de los proporcionados por las notificaciones FPHC. Estos datos se pueden adquirir de las funciones de administración de [eventos de WFP](/windows/desktop/FWP/fwp-mgmt-functions). Estas funciones se muestran en el ejemplo [Mostrar eventos de red.](/windows/desktop/FWP/displaying-net-events)

En el SDK se incluye un ejemplo de administración de eventos más detallado. El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: Archivos de programa SDK de \\ \\ Microsoft Windows Ejemplos \\ \\ <version number> \\ \\ netDs \\ WFP \\ DiagEvents. El Windows SDK de Vista está disponible en el [Centro de descarga.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)

## <a name="built-in-fphc-diagnostics"></a>Diagnósticos FPHC integrados

En ausencia de una extensión FPHC, FPHC puede diagnosticar los escenarios que se enumeran a continuación. La mayoría de los errores de conectividad que diagnostica FPHC se producen porque los firewalls bloquean el tráfico. Los escenarios de IPsec son menos comunes.

En la tabla siguiente se muestran algunos escenarios que provocan errores de conectividad que se pueden diagnosticar mediante FPHC, junto con la información de descripción y reparación que se pasa a NDF.



| Escenario                   | Descripción de estado bajo                                                                                                               | Información de reparación                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Quitar firewall              | La configuración del firewall en este equipo está bloqueando la conexión.                                                                  | Compruebe la configuración del firewall.       |
| Error del modo principal          | No se puede conectar debido a un error de coincidencia de directiva de seguridad de IPsec.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error de modo rápido         | No se puede conectar debido a un error de coincidencia de directiva de seguridad de IPsec.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error en modo de usuario          | No se puede conectar debido a un error de coincidencia de directiva de seguridad de IPsec.                                                                     | Póngase en contacto con el propietario de la directiva IPsec.      |
| Error de credenciales         | No se puede conectar porque la entidad de certificación (CA) raíz de este equipo no coincide con la CA raíz del equipo remoto. | Actualice el certificado raíz de confianza. |
| Certificado expirado        | El certificado usado para la autenticación IPsec ha expirado.                                                                           | Solicitar un certificado.               |
| Otros errores de certificado | No se encontró un certificado válido para la autenticación IPsec.                                                                          | Solicitar un certificado.               |
| Error de Kerberos           | El equipo no forma parte de este dominio.                                                                                             | Unir este equipo a un dominio.      |
| Clave previamente compartida              | Restablezca las claves previamente compartidas.                                                                                                            | Restablezca las claves previamente compartidas.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Plataforma de filtrado de Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Diseño de extensiones de clase auxiliar de NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registro de extensiones de clase auxiliar de NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Ejemplos de clases auxiliares de NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

