---
title: Invocar los archivos dll de extensión
description: Llama a esta función para cada paquete de autenticación o de cuentas válido que recibe del servidor de acceso a la red (NAS).
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995484"
---
# <a name="invoking-the-extension-dlls"></a>Invocar los archivos dll de extensión

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

Los archivos dll de extensión de NPS deben exportar al menos una de las siguientes funciones de devolución de llamada: [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)o [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2). NPS llama a estas funciones para cada paquete de autenticación o de cuentas válido que recibe del servidor de acceso a la red (NAS). NPS llama a estas funciones en cada uno de los archivos DLL que aparecen debajo de la [clave del registro de parámetros](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)de NPS. Se llama a los archivos dll en el orden en que aparecen en la lista.

Si un archivo DLL de extensión de NPS exporta más de una de las funciones anteriores, NPS invoca solo una de ellas: la función más reciente compatible con el sistema operativo.

> [!Note]  
> IAS solo admitía originalmente [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process). IAS también es compatible con [*RadiusExtensionProcessEx*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex). IAS (y NPS posterior) admite también [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2).

 

Los archivos dll de extensión de NPS también pueden exportar funciones [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) y [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) . Si están presentes, NPS llama a estas funciones cuando el servicio se inicia y se detiene, respectivamente.

## <a name="radiusextensionprocess-callback-function"></a>Función de devolución de llamada RadiusExtensionProcess

En un archivo DLL de extensión de autenticación, [*RadiusExtensionProcess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) recibe todos los atributos que NPS recibe en la solicitud de autenticación o de cuentas. Con estos atributos, la función puede realizar validaciones adicionales, comprobar las autorizaciones del usuario o enviar registros de cuentas a un servidor de estado central.

En un archivo DLL de extensión de autorización, **RadiusExtensionProcess** recibe todos los atributos generados por el servicio de autorización de NPS. Estos son los atributos que se devuelven en el paquete de Access-Accept.

Después de llamar a **RadiusExtensionProcess**, la acción que realiza NPS depende del valor devuelto de **RadiusExtensionProcess** y del valor devuelto en el parámetro *pfAction* . Los valores se muestran en la tabla siguiente.



| *pfAction* | DLL de extensión de autenticación                                                                                                                                            | DLL de extensión de autorización                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aceptar     | Omite cualquier dll de extensión de autenticación adicional y también omite el mecanismo de autenticación de NPS.                                                                  | Aceptación no permitida.                                                                                                                                         |
| Reject     | Omite cualquier dll de extensión de autenticación adicional y también omite el mecanismo de autenticación de NPS. Se envía Access-Reject paquete.                                    | Omite cualquier dll de extensión de autorización adicional.                                                                                                          |
| Continuar   | El paquete se envía a la siguiente DLL de extensión de autenticación o al mecanismo de autenticación de NPS si no hay más archivos dll de extensión de autenticación en el registro. | El paquete se envía a la siguiente DLL de extensión de autorización o al registro de cuentas NPS si no se enumeran más archivos dll de extensión de autorización en el registro. |



 

En el caso de todos los archivos dll de extensión, si **RadiusExtensionProcess** devuelve un error, el paquete se descarta. El registro de cuentas NPS no procesa los paquetes que se descartan debido a un error.

Si se produce un error, NPS envía un evento de error genérico al registro de eventos. Se recomienda que el archivo DLL de extensión proporcione un registro de errores adicional.

Para obtener más información y un diagrama que represente el proceso anterior, vea [About NPS Extensions](/windows/desktop/Nps/ias-about-internet-authentication-service).

**RadiusExtensionProcess** debe devolver un error si no puede comprobar la aceptación o el rechazo del paquete. Esta situación puede surgir si un problema de red impide que **RadiusExtensionProcess** se comunique con su base de datos de autenticación de usuario.

Al procesar un paquete de cuentas, el parámetro *pfAction* es **null**, por lo que no se puede establecer *pfAction* . Si se devuelve un error desde la función **RadiusExtensionProcess** al procesar una solicitud de cuentas, NPS descartará la solicitud.

> [!Note]  
> Después de recibir una aceptación, NPS no llama a **RadiusExtensionProcess** en los archivos dll restantes de la secuencia. Dado que algunas funciones de autenticación también pueden implementar autorizaciones, omitir estas funciones de autenticación puede hacer que se omitan las autorizaciones. Si una instancia de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) devuelve Accept, es importante no hacer ninguna suposición sobre las autorizaciones recuperadas.

 

Si se devuelve continue o Accept, el perfil correspondiente al dominio Kerberos se devuelve en el paquete de Access-Accept.

Los archivos dll de extensión de autenticación deben diseñarse para coexistir con los proveedores de autenticación NPS integrados y con otros archivos dll de extensión. Si una extensión solo se puede aplicar a una determinada base de datos de usuario (por ejemplo, Windows Active Directory), debe comprobar el atributo [**ratProvider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) pasado en el parámetro *pAttrs* antes de procesar la solicitud. El atributo ratProvider sería uno de los atributos a los que apunta el parámetro *pAttrs* .

Los archivos dll de extensión no deben rechazar solicitudes porque faltan atributos requeridos. Por ejemplo, si una extensión de autenticación requiere el atributo User-Password, ratUserPassword y el atributo no está presente, la extensión debe devolver una acción de raContinue para proporcionar a otras extensiones y proveedores una oportunidad para procesar la solicitud.

NPS llama a la función [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) después de que se haya tomado la decisión de usar una base de datos de autenticación determinada, pero antes de que el usuario se autentique. Por lo tanto, la información sobre la base de datos de autenticación que se va a utilizar está disponible para la función, de modo que la función puede comprobar las autorizaciones del usuario en la base de datos de autenticación adecuada. NPS admite varias bases de datos de autenticación, incluida la Active Directory de Windows.

## <a name="radiusextensionprocessex-callback-function"></a>Función de devolución de llamada RadiusExtensionProcessEx

Los archivos dll de extensión de NPS pueden exportar [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) en lugar de, o además de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process). Esta función permite que el archivo DLL Anexe atributos de autorización adicionales a la respuesta de autenticación.

La misma información que se describe en la sección de la *función de devolución de llamada RadiusExtensionProcess* se aplica a la función [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) .

[**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) no puede modificar ni quitar ninguno de los atributos que están presentes. Si se produce un escenario en el que la DLL debe modificar o quitar atributos, la única opción es usar la interfaz de usuario de NPS para asegurarse de que los atributos no están presentes. De forma predeterminada, no hay ningún atributo de autorización presente. Cualquier que esté presente se debe haber agregado a través de la interfaz de usuario.

Si se configuran varias dll de autorización y algunas de estas dll implementan [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), la función **RadiusExtensionProcess/ex** de un archivo dll determinado no recibe los atributos de los archivos dll de autorización previamente llamados. Recibe solo los atributos generados por el servicio de autorización de NPS.

## <a name="radiusextensionprocess2-callback-function"></a>Función de devolución de llamada RadiusExtensionProcess2

Los archivos dll de extensión de NPS también pueden exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en lugar de, o además de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) y **RadiusExtensionProcessEx**. Esta función permite que el archivo DLL agregue, modifique y quite atributos de la solicitud o respuesta de autenticación.

La misma información que se describe en la sección de la *función de devolución de llamada RadiusExtensionProcessEx* se aplica a la función [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) , con las siguientes excepciones:

-   En una DLL de autorización, **RadiusExtensionProcess2** recibe los atributos generados por el servicio de autorización NPS y los atributos generados a partir de los archivos dll de autorización previamente llamados.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) no tiene un parámetro *pfAction* . **RadiusExtensionProcess2** establece la disposición final de la solicitud mediante la función [**SetResponseType**](/previous-versions/ms688462(v=vs.85)) proporcionada en la estructura de bloques de [**control de \_ extensión \_ \_ RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .
-   NPS siempre llama a la función [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en cualquier dll restante independientemente de si las funciones de los archivos dll anteriores devolvieron Accept.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de los archivos dll de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 