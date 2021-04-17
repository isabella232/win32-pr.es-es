---
description: Enumera los paquetes de seguridad que se pueden usar con SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Usar paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668123"
---
# <a name="using-security-packages"></a>Usar paquetes de seguridad

La [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) se puede usar con los siguientes [*paquetes de seguridad*](../secgloss/s-gly.md):

-   [Paquete de seguridad de Kerberos](#kerberos-security-package)
-   [Paquete de seguridad de NTLM](#ntlm-security-package)

Los protocolos [*Kerberos*](../secgloss/k-gly.md) y NTLM se implementan como paquetes de seguridad del [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) de Secur32.dll proporcionado con el sistema operativo. De forma predeterminada, la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) carga la compatibilidad con la autenticación Kerberos y NTLM en un equipo cuando se inicia el sistema. En los dominios de Windows Server o Windows, se puede usar cualquiera de los paquetes para autenticar los inicios de sesión de red y las conexiones de cliente/servidor. La que se utiliza depende de las capacidades del equipo en el otro lado de la conexión. Siempre se prefiere el protocolo Kerberos, si está disponible.

Una vez que se ha establecido un contexto de seguridad para un usuario interactivo, se puede cargar otra instancia del paquete Kerberos o NTLM mediante un proceso que se ejecuta en el contexto de seguridad del usuario para admitir el intercambio, la firma, la comprobación, el cifrado y el descifrado de los mensajes. Sin embargo, no se permite el acceso a las [*claves de sesión*](../secgloss/s-gly.md) o a los vales de la memoria caché de credenciales a un proceso distinto de LSA.

Los servicios del sistema y las aplicaciones de nivel de transporte tienen acceso a un SSP a través de SSPI, que proporciona funciones para enumerar los paquetes de seguridad disponibles en un sistema, seleccionar un paquete y usar ese paquete para obtener una conexión autenticada.

Los métodos de SSPI son rutinas genéricas que los programadores pueden usar sin conocer los detalles de un [*Protocolo de seguridad*](../secgloss/s-gly.md)determinado. Por ejemplo, cuando se autentica una conexión cliente/servidor:

1.  La aplicación en el lado cliente de la conexión envía [*las credenciales*](../secgloss/c-gly.md) al servidor mediante la función [**InitializeSecurityContext de SSPI (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
2.  La aplicación en el lado servidor de la conexión responde con la función SSPI [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).
3.  Una vez que se ha autenticado la conexión, la LSA del servidor usa la información del cliente para crear un [*token de acceso*](../secgloss/a-gly.md).
4.  Después, el servidor puede llamar a la función SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para adjuntar el token de acceso a un subproceso de suplantación para el servicio.

## <a name="kerberos-security-package"></a>Paquete de seguridad de Kerberos

El [*paquete de seguridad*](../secgloss/s-gly.md) de Kerberos se basa en el [*Protocolo de autenticación Kerberos*](../secgloss/k-gly.md).

Si se utiliza el protocolo Kerberos para autenticar una conexión cliente/servidor, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) genera un mensaje GSSAPI que incluye un \_ \_ mensaje de solicitud de solicitud de KRB PA desde el cliente. A continuación, [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) genera un mensaje GSSAPI que incluye un \_ mensaje KRB AP \_ REP del servidor.

Para obtener información general sobre los pasos que se realizan en segundo plano en la implementación de un protocolo Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

Todos los servicios distribuidos usan SSPI para tener acceso al protocolo Kerberos. Una lista parcial de las formas en que se usa el protocolo Kerberos para la autenticación incluye:

-   Servicios del administrador de trabajos de impresión
-   Acceso a archivos remotos de CIFS/SMB
-   Consultas [*LDAP*](../secgloss/l-gly.md) en el Active Directory
-   Referencias y administración del sistema de archivos distribuido
-   Autenticación de la entidad de seguridad de host a host de IPsec
-   Solicitudes de reserva para la calidad de servicio de la red
-   Autenticación de intranet en Internet Information Services
-   Administración remota de servidores o estaciones de trabajo mediante RPC autenticado
-   [*Solicitudes de certificado*](../secgloss/c-gly.md) a servicios de Certificate Server para usuarios y equipos del dominio

## <a name="ntlm-security-package"></a>Paquete de seguridad de NTLM

El paquete de seguridad NTLM se basa en el protocolo de autenticación NTLM.

 

 
