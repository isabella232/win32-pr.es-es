---
title: Invocación de los archivos DLL de extensión
description: Llama a estas funciones para cada paquete de autenticación o contabilidad válido que recibe del servidor de acceso a redes (NAS).
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fab05c60ea2ea566f5da76a1c9a3ec9f842641fc19797e85bd51186bc085575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889495"
---
# <a name="invoking-the-extension-dlls"></a>Invocación de los archivos DLL de extensión

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

Los archivos DLL de extensión NPS deben exportar al menos una de las siguientes funciones de devolución de llamada: [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)o [*RadiusExtensionProcess2.*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) NPS llama a esta función para cada paquete de autenticación o contabilidad válido que recibe del servidor de acceso a redes (NAS). NPS llama a estas funciones en cada uno de los archivos DLL enumerados debajo de la clave del [Registro Parameters de](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)NPS. Se llama a los archivos DLL en el orden en que se enumeran.

Si un archivo DLL de extensión NPS exporta más de una de las funciones anteriores, NPS invoca solo una de ellas: la función más reciente compatible con el sistema operativo.

> [!Note]  
> IAS solo admite originalmente [*RadiusExtensionProcess.*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) IAS también admite [*RadiusExtensionProcessEx.*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) IAS (y NPS posteriores) también [*admite RadiusExtensionProcess2.*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)

 

Los archivos DLL de extensión NPS también pueden [**exportar las funciones RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) [**y RadiusExtensionTerm.**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) Si están presentes, NPS llama a estas funciones cuando el servicio se inicia y se detiene, respectivamente.

## <a name="radiusextensionprocess-callback-function"></a>Función de devolución de llamada RadiusExtensionProcess

En un archivo DLL de extensión de [*autenticación, RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) recibe todos los atributos recibidos por NPS en la solicitud de autenticación o contabilidad. Con estos atributos, la función puede realizar validaciones adicionales, comprobar las autorizaciones del usuario o enviar registros de contabilidad a un servidor de estado central.

En un archivo DLL de extensión de autorización, **RadiusExtensionProcess** recibe todos los atributos generados por el servicio de autorización NPS. Estos son los atributos que se devuelven en el Access-Accept paquete.

Después de **llamar a RadiusExtensionProcess**, la acción realizada por NPS depende del valor devuelto de **RadiusExtensionProcess** y del valor devuelto en el *parámetro pfAction.* Los valores se muestran en la tabla siguiente.



| *pfAction* | DLL de extensión de autenticación                                                                                                                                            | ARCHIVO DLL de extensión de autorización                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aceptar     | Omite los archivos DLL de extensión de autenticación adicionales y también omite el mecanismo de autenticación de NPS.                                                                  | No se permite aceptar.                                                                                                                                         |
| Reject     | Omite los archivos DLL de extensión de autenticación adicionales y también omite el mecanismo de autenticación de NPS. Access-Reject paquete se envía.                                    | Omite cualquier archivo DLL de extensión de autorización adicional.                                                                                                          |
| Continuar   | El paquete se envía al siguiente archivo DLL de extensión de autenticación o al mecanismo de autenticación nps si no se muestran más archivos DLL de extensión de autenticación en el registro. | El paquete se envía al siguiente archivo DLL de la extensión de autorización o al registro de contabilidad de NPS si no aparecen más archivos DLL de extensión de autorización en el Registro. |



 

Para todos los archivos DLL de extensión, **si RadiusExtensionProcess** devuelve un error, se descarta el paquete. El registro de contabilidad de NPS no procesa los paquetes que se descartan debido a un error.

Si se produce un error, NPS envía un evento de error genérico al registro de eventos. Se recomienda que el archivo DLL de extensión proporcione un registro de errores adicional.

Para obtener más información y un diagrama que representa el proceso anterior, vea [Acerca de las extensiones NPS](/windows/desktop/Nps/ias-about-internet-authentication-service).

**RadiusExtensionProcess debe** devolver un error si no puede comprobar la aceptación o rechazo del paquete. Esta situación puede surgir si un problema de red impide **que RadiusExtensionProcess** se comunique con su base de datos de autenticación de usuario.

Al procesar un paquete de contabilidad, el *parámetro pfAction* es **NULL,** por lo que no se puede establecer *pfAction.* Devolver un error de la **función RadiusExtensionProcess** al procesar una solicitud de contabilidad hace que NPS descarte la solicitud.

> [!Note]  
> Después de recibir una aceptación, NPS no llama a **RadiusExtensionProcess** en los archivos DLL restantes de la secuencia. Dado que algunas funciones de autenticación también pueden implementar autorizaciones, la omisión de estas funciones de autenticación puede provocar la omisión de las autorizaciones. Si una instancia de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) devuelve Accept, es importante no realizar suposiciones sobre las autorizaciones recuperadas.

 

Si se devuelve Continue o Accept, el perfil correspondiente al dominio kerberos se devuelve en el Access-Accept paquete.

Los archivos DLL de extensión de autenticación deben estar diseñados para coexistir con los proveedores de autenticación de NPS integrados y con otros archivos DLL de extensión. Si una extensión solo es aplicable a una base de datos de usuario determinada (por ejemplo, Windows Active Directory), debe comprobar el [**atributoprovider pasado**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) en el *parámetro pAttrs* antes de procesar la solicitud. El atributoprovider sería una de una lista de atributos a los que apunta el *parámetro pAttrs.*

Los archivos DLL de extensión no deben rechazar las solicitudes porque faltan los atributos necesarios. Por ejemplo, si una extensión de autenticación requiere el atributo User-Password,userUserPassword y el atributo no está presente, la extensión debe devolver una acción de raContinue para dar a otras extensiones y proveedores la oportunidad de procesar la solicitud.

NPS llama a la [**función RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) después de tomar la decisión de usar una base de datos de autenticación determinada, pero antes de que el usuario se autentique. Por lo tanto, la información sobre la base de datos de autenticación que se va a usar está disponible para la función, de modo que la función pueda comprobar las autorizaciones del usuario en la base de datos de autenticación adecuada. NPS admite varias bases de datos de autenticación, Windows Active Directory.

## <a name="radiusextensionprocessex-callback-function"></a>Función de devolución de llamada RadiusExtensionProcessEx

Los archivos DLL de extensión NPS pueden [**exportar RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) en lugar de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)o además de . Esta función permite que el archivo DLL anexe atributos de autorización adicionales a la respuesta de autenticación.

La misma información descrita en la sección Función de devolución de llamada *RadiusExtensionProcess* se aplica a la [**función RadiusExtensionProcessEx.**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) no puede modificar ni quitar ninguno de los atributos que están presentes. Si surge un escenario en el que el archivo DLL debe modificar o quitar atributos, la única opción es usar la interfaz de usuario nps para asegurarse de que los atributos no están presentes. De forma predeterminada, no hay atributos de autorización presentes. Los que estén presentes se deben haber agregado a través de la interfaz de usuario.

Si se configuran varios archivos DLL de autorización y algunos de estos archivos DLL implementan [**RadiusExtensionProcessEx,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)la función **RadiusExtensionProcess/Ex** de un archivo DLL determinado no recibe los atributos de los archivos DLL de autorización anteriormente denominados. Recibe solo los atributos generados por el servicio de autorización NPS.

## <a name="radiusextensionprocess2-callback-function"></a>Función de devolución de llamada RadiusExtensionProcess2

Los archivos DLL de extensión NPS también pueden exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en lugar de o además de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) y **RadiusExtensionProcessEx.** Esta función permite que el archivo DLL agregue, modifique y quite atributos a y desde la solicitud o respuesta de autenticación.

La misma información descrita en la sección Función de devolución de llamada *RadiusExtensionProcessEx* se aplica a la [**función RadiusExtensionProcess2,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) con las siguientes excepciones:

-   En un archivo DLL de autorización, **RadiusExtensionProcess2** recibe los atributos generados por el servicio de autorización NPS y los atributos generados a partir de archivos DLL de autorización anteriormente denominados DLL de autorización.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) no tiene un *parámetro pfAction.* **RadiusExtensionProcess2 establece** la disposición final de la solicitud mediante la [**función SetResponseType**](/previous-versions/ms688462(v=vs.85)) proporcionada en la [**estructura RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK.**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)
-   NPS siempre llama a la [**función RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en los archivos DLL restantes, independientemente de si las funciones de los archivos DLL anteriores devolvieron Accept.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de los archivos DLL de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 