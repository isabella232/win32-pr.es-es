---
title: Autenticación (API de servidor HTTP)
description: A partir de la versión 2.0, la API del servidor HTTP realiza la autenticación del lado servidor para la aplicación.
ms.assetid: e8e41e8e-1b10-4747-b18e-763e0752ade4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4e3c35dc4e244fd51af42bb3c52d225d233364f61fc79a8127ef450e84016fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078365"
---
# <a name="authentication-http-server-api"></a>Autenticación (API de servidor HTTP)

Algunas aplicaciones de servidor requieren autenticación de cliente para acceder a recursos y solicitudes HTTP de servicio. A partir de la versión 2.0, la API del servidor HTTP realiza la autenticación del lado servidor para la aplicación. En la versión 1.0 de LA API del servidor HTTP, la aplicación de servidor tenía que implementar su propia autenticación. Entre las ventajas de la autenticación realizada por la API del servidor HTTP se incluyen las siguientes:

-   Las aplicaciones se pueden ejecutar con pocos privilegios, lo que reduce los riesgos de seguridad.
-   La autenticación se realiza en modo kernel, lo que reduce las transiciones del modo de usuario al modo kernel durante la autenticación.
-   La autenticación realizada en modo kernel permite que las aplicaciones de servidor se ejecuten en diferentes cuentas de usuario. En la versión 1.0, todas las aplicaciones del equipo deben ejecutarse en la misma cuenta de usuario para autenticarse en el nombre principal de servicio (SPN).
-   El protocolo de enlace de autenticación NTLM no se restablece si se recicla un proceso de trabajo mientras el protocolo de enlace está en proceso.

Para aprovechar las ventajas de la autenticación de la versión 2.0, la aplicación habilita los esquemas de autenticación que la API del servidor HTTP aplica a las direcciones URL para las que se ha registrado la aplicación. La autenticación se puede habilitar en la sesión del servidor o en el grupo de direcciones URL. El grupo de direcciones URL hereda los esquemas de autenticación habilitados por la sesión del servidor si no se establece ninguno en el grupo de direcciones URL. La API del servidor HTTP admite los siguientes esquemas:

-   Negotiate
-   NTLM
-   Digest
-   Básico

La aplicación de servidor también puede implementar esquemas de autenticación no admitidos por la API del servidor HTTP. La API del servidor HTTP envía solicitudes a la aplicación para esquemas de autenticación que no se admiten o para esquemas que la aplicación no ha habilitado.

### <a name="enabling-authentication"></a>Habilitar la autenticación

La aplicación de servidor habilita y configura la autenticación en la sesión del servidor o el grupo de direcciones URL con las funciones [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) de la siguiente manera:

1.  La aplicación habilita la autenticación **especificando HttpServerAuthenticationProperty en** el parámetro *Property* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).
2.  La aplicación especifica los parámetros de configuración en la estructura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) en el *parámetro pPropertyInformation* de [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). La aplicación especifica los esquemas de autenticación habilitados, independientemente de si el almacenamiento en caché de credenciales NTLM está deshabilitado, y proporciona los parámetros Básico e Implícita en la estructura **HTTP \_ SERVER AUTHENTICATION \_ \_ INFO.**

### <a name="authentication-procedure"></a>Procedimiento de autenticación

Para iniciar la autenticación del servidor HTTP, la aplicación habilita la propiedad de autenticación antes de que la primera solicitud llegue a la cola de solicitudes. Los pasos siguientes son el flujo de procesamiento común para autenticar una solicitud.

1.  La aplicación habilita la autenticación. Consulte la sección anterior "Habilitación de la autenticación".
    > [!Note]  
    > El cliente envía una solicitud no autenticada. La API del servidor HTTP pasa la solicitud a la aplicación de servidor y le permite generar el desafío 401 inicial. La API del servidor HTTP incluye la [**estructura HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) insertada con la [**estructura HTTP \_ REQUEST.**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) El **miembro AuthStatus** indica **HttpAuthStatusNotAuthenticated**

     

2.  La aplicación examina el miembro **AuthStatus** de la estructura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar si la solicitud se ha autenticado. Si la solicitud no se ha autenticado, la aplicación puede realizar la solicitud como anónima o enviar un desafío de autenticación 401 inicial.
3.  Si la aplicación atiende la solicitud como anónima, controla la solicitud y envía la respuesta final a la aplicación cliente, como si la autenticación no se hubiera implicado.
4.  Si, en su lugar, la aplicación requiere autenticación, envía el desafío 401 inicial con uno o varios encabezados WWW-Authenticate que indican los esquemas disponibles para el cliente. La aplicación debe usar la estructura [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para compilar el conjunto necesario de encabezados cuando se envía más de un encabezado de autenticación en la respuesta.
    > [!Note]
    >
    > El cliente vuelve a enviar la solicitud con el encabezado de autorización para un esquema seleccionado del conjunto de esquemas disponibles indicados por la aplicación de servidor en la respuesta 401 inicial.
    >
    > La API del servidor HTTP examina el encabezado de autorización de la solicitud de autorización para determinar si el esquema está habilitado. Si es así, la API del servidor HTTP realiza la autenticación y controla todos los intercambios provisionales de solicitud/401-respuesta, hasta que se completa el protocolo de enlace de autenticación.
    >
    > Cuando la API del servidor HTTP completa el intento de autenticación, envía la solicitud a la aplicación con los resultados del intento de autenticación en la estructura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) que se devuelve con la solicitud. Si se produce un error en el intento de autenticación por uno de los siguientes motivos, la API del servidor HTTP no pasa la solicitud a la aplicación:
    >
    > -   Si se produce un error en el protocolo de enlace de autenticación debido a un error interno de la API del servidor HTTP, como un error de asignación de memoria, la API del servidor HTTP genera una respuesta 503 (servicio no disponible) y se envía de vuelta al cliente.
    > -   Si se encuentra un encabezado de autorización con un formato malformado, como un encabezado sin un nombre de esquema o una codificación Base64 de credenciales de cliente con un formato de error, la API del servidor HTTP genera una respuesta 400 (solicitud no válida) y la devuelve al cliente.

     

5.  La aplicación de servidor examina el miembro **AuthStatus** de la estructura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para determinar si la autenticación se ha realizado correctamente. Cuando se produce un error en la autenticación, la API del servidor HTTP incluye el error devuelto por [AcceptSecurityContext](/previous-versions/windows/embedded/ms937012(v=msdn.10)) en el **miembro SecStatus** de la estructura **HTTP REQUEST \_ \_ AUTH \_ INFO.** Si se produce un error en el intento de autenticación debido a credenciales no válidas, la aplicación puede generar otro desafío 401 con el encabezado WWW-Authenticate deseado o puede decidir dar servicio a la solicitud como anónima.
6.  Si la autenticación se ha realizado correctamente, la aplicación usa el token proporcionado en la estructura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) para suplantar al cliente y acceder a los recursos. El identificador del token de acceso devuelto a la aplicación es válido siempre que el identificador de solicitud sea válido, que suele ser hasta que la aplicación completa la respuesta a la solicitud. Sin embargo, el token puede expirar durante este período y es posible que la aplicación tenga que enviar otro desafío 401 al cliente.
7.  La aplicación envía la respuesta 200 OK final y debe cerrar el identificador al token de acceso.
    > [!Note]  
    > La API del servidor HTTP anexa los datos de autenticación mutua a la respuesta 200 OK final, si se generó uno durante el protocolo de enlace de autenticación.

     

### <a name="ntlm-null-sessions"></a>Sesiones NULL NTLM

Tenga en cuenta que una sesión NTLM NULL indicada en el contexto de seguridad final no se trata como autenticada. En este caso, la solicitud se envía a la aplicación con un error HttpAuthStatusFailure en la estructura [**HTTP \_ REQUEST \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) y la aplicación puede enviar otro desafío 401.

### <a name="preemptive-authentication"></a>Autenticación preferente

Según el protocolo HTTP, una vez que el cliente ha establecido la autenticación para un recurso, puede enviar de forma preferente el encabezado de autorización correspondiente con solicitudes consecutivas posteriores para el recurso sin tener que esperar un desafío 401 del servidor. Si el esquema indicado en el encabezado Autorización sigue habilitado por la aplicación y es compatible con la API del servidor HTTP, el servidor HTTP intenta la autenticación sin enviar la solicitud a la aplicación. Cuando la aplicación recibe este tipo de solicitud autenticada, puede optar por descartar la solicitud y volver a generar el desafío 401 inicial o dar servicio a la solicitud como autenticada.

### <a name="mutual-authentication"></a>Autenticación mutua

Los datos de autenticación mutua se generan cuando se usa el esquema de negociación durante el protocolo de enlace y se resuelven en Kerberos, y el cliente ha solicitado autenticación mutua. La API de servidor HTTP inserta automáticamente los datos de autenticación mutua en la respuesta 200 OK final enviada por la aplicación de servidor. De forma predeterminada, la API de servidor HTTP no pasa los datos de autenticación mutua a la aplicación de servidor, ya que controla automáticamente el envío de los datos. Sin embargo, si la aplicación de servidor habilita la marca ReceiveMutualAuth en la estructura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) en la configuración, los datos de autenticación mutua se pasan a la aplicación en la estructura [**HTTP REQUEST \_ \_ AUTH \_ INFO**](/windows/desktop/api/Http/ns-http-http_request_auth_info) insertada con la SOLICITUD HTTP autenticada. [**\_**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) En este caso, la aplicación debe enviar los datos de autenticación mutua con la respuesta 200 OK final. En el caso de que un único equipo abate varios sitios, todos los sitios del equipo usan las credenciales de la cuenta de equipo local en el dominio para la autenticación mutua.

 

 
