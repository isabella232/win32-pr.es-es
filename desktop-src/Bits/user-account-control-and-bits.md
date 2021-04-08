---
title: Control de cuentas de usuario y BITS
description: Cuando un usuario administrador inicia sesión en el equipo, se crean dos tokens de acceso. Uno es un token de acceso de usuario estándar filtrado y el otro es un token de acceso de administrador completo.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 3017b3a0d816ba393d1427c5c1d2315a68b2dcc0
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2020
ms.locfileid: "103995027"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Seguridad de BITS, tokens y cuentas de administrador

## <a name="http-server-certificate-callbacks"></a>Devoluciones de llamada de certificado de servidor HTTP
La validación correcta de los certificados de servidor es una parte fundamental del mantenimiento de la seguridad HTTPS. BITS ayuda a validar siempre los certificados de servidor con una lista de requisitos especificados por [**SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). De forma predeterminada, BITS usa la validación de certificados de estilo "explorador".

También puede especificar una función personalizada a la que llamar para validar más el certificado. Establezca la devolución de llamada del certificado de servidor con el método [**SetServerCertificateValidationInterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) . Solo se llamará al método después de que el sistema operativo haya validado el certificado basándose en la llamada [ **SetSecurityFlag** s](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) . 

## <a name="http-client-certificates"></a>Certificados de cliente HTTP
Puede establecer un certificado de cliente en un trabajo HTTP con dos métodos diferentes de configuración de certificado. Puede establecer un certificado por el [identificador](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o por el nombre de [sujeto](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)del certificado. El certificado de cliente se utilizará durante la negociación de TLS (o la renegociación) si el servidor requiere la autenticación del cliente.

## <a name="write-only-http-headers"></a>Encabezados HTTP de solo escritura
BITS le ayuda a proteger los tokens de autenticación HTTP del acceso no deseado. A menudo, un servidor HTTP necesitará algún tipo de token de seguridad o cadena al descargar o cargar un archivo en servidores HTTP.

BITS protege estos tokens de autenticación de varias maneras.
* BITS le permite usar conexiones HTTP protegidas por SSL y TLS especificando una dirección URL HTTPS.
* Los encabezados personalizados siempre se conservan en un formato cifrado en el disco.
* Puede evitar que los encabezados de cliente se devuelvan a otros programas con el método [**IBackgroundCopyJobHttpOptions3:: MakeCustomHeadersWriteOnly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) .


## <a name="standard-and-administrator-users"></a>Usuarios estándar y de administrador
Un usuario que esté en el grupo de administradores puede ejecutar un proceso con acceso de usuario estándar o en un estado elevado (con privilegios de administrador). BITS ejecutará el trabajo en cualquier estado siempre que el usuario haya iniciado sesión en el equipo. Sin embargo, si el usuario creó el trabajo o tomó posesión del trabajo en un estado elevado, el usuario debe tener el estado elevado para recuperar o modificar el trabajo (de lo contrario, se produce un error en la llamada con acceso denegado (0x80070005)). Para determinar el estado con privilegios elevados de un trabajo, llame al método [**IBackgroundCopyJob4:: GetOwnerElevationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) .

Un usuario estándar no puede enumerar ni modificar trabajos que pertenecen a otros usuarios.

## <a name="integrity-level"></a>Nivel de integridad
Además del estado elevado, el nivel de integridad del token puede determinar si el usuario puede modificar un trabajo. Un cliente no puede modificar trabajos creados por un token con un nivel de integridad superior. En concreto, muchos tokens del sistema local llevan un nivel de integridad mayor que el nivel de integridad de una ventana con privilegios elevados, por lo que un administrador no puede modificarlos desde una ventana de comandos normal con privilegios elevados. Por ejemplo, Windows Update y los trabajos de SMS se ejecutan como LocalSystem, que tiene un nivel de integridad mayor que un token con privilegios elevados, por lo que un administrador no puede modificar ni eliminar estos trabajos. Para modificar estos trabajos, cree una tarea Programador de tareas que se ejecute como sistema local. La tarea puede ejecutar una aplicación de consola que usa la API de BITS, o bien la tarea podría ejecutar un script que llama a BitsAdmin.exe. Para determinar el nivel de integridad usado, llame al método [**IBackgroundCopyJob4:: GetOwnerIntegrityLevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) .

## <a name="service-identity"></a>Identidad de servicio
A partir de la actualización 2019 de mayo de Windows 10 (10,0; Compilación 18362), los trabajos de BITS iniciados desde un servicio conservarán la identidad del servicio. Esto permite que los servicios que desean usar BITS descarguen o carguen archivos de un directorio cuyos permisos están vinculados al SID del servicio. Además, el tráfico de red se atribuye correctamente al servicio que solicitó el trabajo de BITS en lugar de atribuirse a BITS.

 




