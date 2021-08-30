---
title: Control de cuentas de usuario y BITS
description: Cuando un usuario administrador inicia sesión en el equipo, se crean dos tokens de acceso. Uno es un token de acceso de usuario estándar filtrado y el otro es un token de acceso de administrador completo.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 1893c9abc9d783cea6b8ff17e5bcbef47cfc613890c97b45530257950659887d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004685"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Seguridad, tokens y cuentas de administrador de BITS

## <a name="http-server-certificate-callbacks"></a>Devoluciones de llamada de certificado de servidor HTTP
Validar correctamente los certificados de servidor es una parte clave del mantenimiento de la seguridad HTTPS. BITS ayuda a validar siempre los certificados de servidor con una lista de requisitos especificados [**por SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). De forma predeterminada, BITS usa la validación de certificados de estilo "explorador".

También puede especificar una función personalizada a la que llamar para validar aún más el certificado. Establezca la devolución de llamada del certificado de servidor [**con el método SetServerCertificateValidationInterface.**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) Solo se llamará al método después de que el sistema operativo haya validado el certificado en función de la llamada a [ **SetSecurityFlag.**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) 

## <a name="http-client-certificates"></a>Certificados de cliente HTTP
Puede establecer un certificado de cliente en un trabajo HTTP con dos métodos de configuración de certificado diferentes. Puede establecer un certificado por identificador [o](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) por el nombre de sujeto [del certificado](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname). El certificado de cliente se usará durante la negociación de TLS (o renegociación) si el servidor requiere autenticación de cliente.

## <a name="write-only-http-headers"></a>Encabezados HTTP de solo escritura
BITS ayuda a proteger los tokens de autenticación HTTP frente al acceso no deseado. A menudo, un servidor HTTP necesitará algún tipo de token o cadena de seguridad al descargar o cargar un archivo en servidores HTTP.

BITS protege estos tokens de autenticación de varias maneras.
* BITS permite usar conexiones HTTP protegidas con TLS y SSL especificando una dirección URL HTTPS.
* Los encabezados personalizados siempre se conservan en un formato cifrado en disco.
* Puede evitar que los encabezados de cliente se devuelvan a otros programas con el método [**IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly.**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly)


## <a name="standard-and-administrator-users"></a>Usuarios estándar y administrador
Un usuario que se encuentra en el grupo de administradores puede ejecutar un proceso con acceso de usuario estándar o en un estado elevado (con privilegios de administrador). BITS ejecutará el trabajo en cualquier estado siempre y cuando el usuario haya iniciado sesión en el equipo. Sin embargo, si el usuario creó el trabajo o tomó posesión del trabajo en un estado elevado, el usuario debe estar en el estado con privilegios elevados para recuperar o modificar el trabajo (de lo contrario, se produce un error en la llamada con acceso denegado (0x80070005)). Para determinar el estado elevado de un trabajo, llame al [**método IBackgroundCopyJob4::GetOwnerExiaationState.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate)

Un usuario estándar no puede enumerar ni modificar trabajos propiedad de otros usuarios.

## <a name="integrity-level"></a>Nivel de integridad
Además del estado elevado, el nivel de integridad del token puede determinar si el usuario puede modificar un trabajo. Un cliente no puede modificar los trabajos creados por un token con un nivel de integridad superior. En concreto, muchos tokens del sistema local tienen un nivel de integridad superior al nivel de integridad de una ventana con privilegios elevados, por lo que un administrador no puede modificarlo desde una ventana de comandos con privilegios elevados normales. Por ejemplo, los Windows update y SMS se ejecutan como LocalSystem, que tiene un nivel de integridad mayor que un token con privilegios elevados, por lo que un administrador no puede modificar ni eliminar estos trabajos. Para modificar estos trabajos, cree una Programador de tareas que se ejecute como sistema local. La tarea puede ejecutar una aplicación de consola que usa la API de BITS o la tarea podría ejecutar un script que llame a BitsAdmin.exe. Para determinar el nivel de integridad utilizado, llame al [**método IBackgroundCopyJob4::GetOwnerIntegrityLevel.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel)

## <a name="service-identity"></a>Identidad de servicio
A partir de Actualización de mayo de 2019 de Windows 10 (10.0; Compilación 18362), los trabajos de BITS iniciados desde un servicio mantendrán la identidad del servicio. Esto permite a los servicios que desean usar BITS para descargar o cargar archivos desde un directorio cuyos permisos están asociados al SID del servicio. Además, el tráfico de red se atribuirá correctamente al servicio que solicitó el trabajo de BITS en lugar de atribuirse a BITS.

 




