---
title: Autenticación (API de servidor HTTP)
description: A partir de la versión 2,0, la API del servidor HTTP realiza la autenticación del lado servidor para la aplicación.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d523df90861c83a45f67811edad243ceee5165
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421805"
---
# <a name="authentication-http-server-api"></a>Autenticación (API de servidor HTTP)

Algunas aplicaciones de servidor requieren la autenticación del cliente para tener acceso a los recursos y las solicitudes HTTP del servicio. A partir de la versión 2,0, la API del servidor HTTP realiza la autenticación del lado servidor para la aplicación. En la API del servidor HTTP versión 1,0, la aplicación de servidor tenía que implementar su propia autenticación. Entre las ventajas de la autenticación realizada por la API del servidor HTTP se incluyen las siguientes:

-   Las aplicaciones se pueden ejecutar con pocos privilegios, lo que reduce los riesgos de seguridad.
-   La autenticación se realiza en modo kernel, lo que reduce las transiciones del modo de usuario al modo kernel durante la autenticación.
-   La autenticación realizada en modo kernel permite que las aplicaciones de servidor se ejecuten en diferentes cuentas de usuario. En la versión 1,0, todas las aplicaciones de la máquina deben ejecutarse en la misma cuenta de usuario para autenticarse en el nombre principal del servicio (SPN).
-   El protocolo de enlace de autenticación NTLM no se restablece si un proceso de trabajo se recicla mientras el protocolo de enlace está en curso.

Para aprovechar la autenticación de la versión 2,0, la aplicación habilita los esquemas de autenticación que la API del servidor HTTP aplica a las direcciones URL para las que se ha registrado la aplicación. La autenticación se puede habilitar en el grupo de URL o la sesión del servidor. El grupo de direcciones URL hereda los esquemas de autenticación habilitados por la sesión del servidor si no se establece ninguno en el grupo de direcciones URL. La API del servidor HTTP admite los siguientes esquemas:

-   Negotiate
-   NTLM
-   Digest
-   Básico

La aplicación de servidor también puede implementar esquemas de autenticación no admitidos por la API del servidor HTTP. La API del servidor HTTP envía las solicitudes a la aplicación para los esquemas de autenticación que no se admiten o para los esquemas que no se han habilitado en la aplicación.

### <a name="enabling-authentication"></a>Habilitar la autenticación

La aplicación de servidor habilita y configura la autenticación en la sesión de servidor o el grupo de direcciones URL con las funciones [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) de la siguiente manera:

1.  La aplicación habilita la autenticación mediante la especificación de **HttpServerAuthenticationProperty** en el parámetro *Property* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  La aplicación especifica los parámetros de configuración en la estructura de [**información de autenticación del \_ servidor \_ \_ http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) en el parámetro *pPropertyInformation* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). La aplicación especifica los esquemas de autenticación habilitados, si está deshabilitado el almacenamiento en caché de credenciales NTLM y proporciona los parámetros básicos y de resumen en la estructura de **\_ información de \_ autenticación \_ del servidor http** .

### <a name="authentication-procedure"></a>Procedimiento de autenticación

Para iniciar la autenticación de servidor HTTP, la aplicación habilita la propiedad de autenticación antes de que llegue la primera solicitud a la cola de solicitudes. Los pasos siguientes son el flujo de procesamiento común para autenticar una solicitud.

1.  La aplicación habilita la autenticación. Vea la sección anterior "habilitación de la autenticación".
    > [!Note]  
    > El cliente envía una solicitud no autenticada. La API del servidor HTTP pasa la solicitud a la aplicación de servidor y permite generar el desafío inicial de 401. La API del servidor HTTP incluye la estructura de información de autenticación de la [**\_ solicitud \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) insertada con la estructura de la [**\_ solicitud HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) . El miembro **AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  La aplicación examina el miembro **AuthStatus** de la estructura [**de \_ \_ \_ información de autenticación de la solicitud HTTP**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar si se ha autenticado la solicitud. Si la solicitud no se ha autenticado, la aplicación puede atender la solicitud como anónima o enviar un desafío de autenticación 401 inicial.
3.  Si la aplicación atiende la solicitud como anónima, controla la solicitud y envía la respuesta final a la aplicación cliente, al igual que si la autenticación no estuviera implicada.
4.  Si en su lugar la aplicación requiere autenticación, envía el desafío inicial 401 con uno o varios encabezados de WWW-Authenticate que indican los esquemas disponibles para el cliente. La aplicación debe utilizar la estructura [**http \_ Multiple \_ knowd \_ headers**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para compilar el conjunto necesario de encabezados cuando se envía más de un encabezado de autenticación en la respuesta.
    > [!Note]
    >
    > El cliente vuelve a enviar la solicitud con el encabezado de autorización para un esquema seleccionado en el conjunto de esquemas disponibles indicado por la aplicación de servidor en la respuesta inicial 401.
    >
    > La API del servidor HTTP examina el encabezado de autorización de solicitud de autorización para determinar si el esquema está habilitado. Si es así, la API del servidor HTTP realiza la autenticación y controla todos los intercambios provisionales de solicitud/401-respuesta hasta que finalice el protocolo de enlace de autenticación.
    >
    > Cuando la API del servidor HTTP completa el intento de autenticación, envía la solicitud a la aplicación con los resultados del intento de autenticación en la estructura de [**\_ \_ \_ información**](/windows/desktop/api/Http/ns-http-http_request_auth_info) de autenticación de la solicitud HTTP que se devuelve con la solicitud. Si se produce un error en el intento de autenticación por una de las razones siguientes, la API del servidor HTTP no pasa la solicitud a la aplicación:
    >
    > -   Si se produce un error en el protocolo de enlace de autenticación debido a un error interno de la API del servidor HTTP, como un error de asignación de memoria, la API del servidor HTTP genera una respuesta 503 (servicio no disponible) y vuelve a enviar al cliente.
    > -   Si un encabezado de autorización con formato incorrecto, como un encabezado sin nombre de esquema, o la codificación Base64 con formato incorrecto de las credenciales de cliente encontradas, la API del servidor HTTP genera una respuesta 400 (solicitud incorrecta) y vuelve a enviar al cliente.

     

5.  La aplicación de servidor examina el miembro **AuthStatus** de la estructura de información de autenticación de la [**\_ solicitud \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar si la autenticación fue correcta. Cuando se produce un error de autenticación, la API del servidor HTTP incluye el error devuelto por [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) en el miembro **SecStatus** de la estructura de información de autenticación de la **\_ solicitud \_ \_ http** . Si se produce un error en el intento de autenticación debido a credenciales no válidas, la aplicación puede generar otro desafío 401 con el encabezado de WWW-Authenticate deseado o puede decidir atender la solicitud como anónima.
6.  Si la autenticación se realizó correctamente, la aplicación usa el token proporcionado en la estructura de información de autenticación de la [**\_ solicitud \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para suplantar al cliente y obtener acceso a los recursos. El identificador de token de acceso que se devuelve a la aplicación es válido siempre que el identificador de solicitud sea válido, que suele ser hasta que la aplicación completa la respuesta a la solicitud. No obstante, el token puede expirar durante este período y es posible que la aplicación necesite enviar otro desafío 401 al cliente.
7.  La aplicación envía la respuesta final de 200 aceptar y debe cerrar el identificador del token de acceso.
    > [!Note]  
    > La API del servidor HTTP anexa los datos de autenticación mutua a la respuesta final de 200 correcto, si se generó una durante el protocolo de enlace de autenticación.

     

### <a name="ntlm-null-sessions"></a>Sesiones NULAs de NTLM

Tenga en cuenta que una sesión nula NTLM indicada en el contexto de seguridad final no se trata como autenticada. En este caso, la solicitud se envía a la aplicación con un error HttpAuthStatusFailure en la estructura de información de autenticación de la [**\_ solicitud \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) y la aplicación puede enviar otro desafío 401.

### <a name="preemptive-authentication"></a>Autenticación preferente

Según el protocolo HTTP, una vez que el cliente ha establecido la autenticación de un recurso, puede enviar de forma preferente el encabezado de autorización correspondiente con las solicitudes consecutivas posteriores para el recurso sin esperar un desafío 401 desde el servidor. Si el esquema indicado en el encabezado de autorización sigue estando habilitado por la aplicación y admitido por la API del servidor HTTP, el servidor HTTP intentará la autenticación sin enviar la solicitud a la aplicación. Cuando la aplicación recibe este tipo de solicitud autenticada, puede optar por descartar la solicitud y volver a generar el desafío 401 inicial o el servicio de la solicitud como autenticado.

### <a name="mutual-authentication"></a>Autenticación mutua

Los datos de autenticación mutua se generan cuando se usa el esquema Negotiate durante el protocolo de enlace y se resuelve en Kerberos, y el cliente ha solicitado la autenticación mutua. Los datos de autenticación mutua se insertan automáticamente mediante la API del servidor HTTP en la respuesta final 200 aceptar enviada por la aplicación de servidor. De forma predeterminada, la API de servidor HTTP no pasa los datos de autenticación mutua a la aplicación de servidor, ya que controla automáticamente el envío del mismo. Sin embargo, si la aplicación de servidor habilita la marca ReceiveMutualAuth en la estructura de [**\_ información de \_ autenticación \_ del servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) en la configuración, los datos de autenticación mutua se pasan a la aplicación en la estructura de información de autenticación de [**\_ solicitud \_ \_ http**](/windows/desktop/api/Http/ns-http-http_request_auth_info) insertada con la [**\_ solicitud HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))autenticada. En este caso, la aplicación debe enviar los datos de autenticación mutua con la respuesta 200 aceptar final. En el caso de que un único equipo atienda varios sitios, todos los sitios del equipo utilizan las credenciales de la cuenta del equipo local en el dominio para la autenticación mutua.

 

 
