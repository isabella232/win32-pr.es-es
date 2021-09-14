---
description: Enumera los paquetes de seguridad que se pueden usar con SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Uso de paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160897"
---
# <a name="using-security-packages"></a>Uso de paquetes de seguridad

La [*interfaz del proveedor de compatibilidad de*](../secgloss/s-gly.md) seguridad (SSPI) se puede usar con los siguientes [*paquetes de seguridad:*](../secgloss/s-gly.md)

-   [Paquete de seguridad de Kerberos](#kerberos-security-package)
-   [Paquete de seguridad NTLM](#ntlm-security-package)

Los [*protocolos Kerberos*](../secgloss/k-gly.md) y NTLM se implementan como paquetes de seguridad del proveedor de compatibilidad de seguridad (SSP) de Secur32.dll proporcionado con el sistema operativo. [](../secgloss/s-gly.md) De forma predeterminada, la autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) carga la compatibilidad con la autenticación Kerberos y NTLM en un equipo cuando se inicia el sistema. En Windows server o Windows, se puede usar cualquier paquete para autenticar los inicios de sesión de red y las conexiones de cliente/servidor. El que se usa depende de las funciones del equipo en el otro lado de la conexión. Siempre se prefiere el protocolo Kerberos, si está disponible.

Una vez establecido un contexto de seguridad para un usuario interactivo, un proceso que se ejecuta en el contexto de seguridad del usuario puede cargar otra instancia del paquete Kerberos o NTLM para admitir el intercambio, la firma, la comprobación, el cifrado y el descifrado de mensajes. Sin embargo, ningún proceso que no sea el LSA nunca tiene permitido el acceso a claves [*de sesión o*](../secgloss/s-gly.md) vales en la memoria caché de credenciales.

Los servicios del sistema y las aplicaciones de nivel de transporte acceden a un SSP a través de SSPI, que proporciona funciones para enumerar los paquetes de seguridad disponibles en un sistema, seleccionar un paquete y usar ese paquete para obtener una conexión autenticada.

Los métodos de SSPI son rutinas genéricas que los desarrolladores pueden usar sin conocer los detalles de un protocolo [*de seguridad determinado.*](../secgloss/s-gly.md) Por ejemplo, cuando se autentica una conexión cliente/servidor:

1.  La aplicación del lado cliente de la conexión [*envía*](../secgloss/c-gly.md) credenciales al servidor mediante la función de SSPI [**InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  La aplicación del lado servidor de la conexión responde con la función de SSPI [**AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  Una vez autenticada la conexión, el LSA del servidor usa información del cliente para crear un [*token de acceso.*](../secgloss/a-gly.md)
4.  A continuación, el servidor puede llamar a la función [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) de SSPI para adjuntar el token de acceso a un subproceso de suplantación para el servicio.

## <a name="kerberos-security-package"></a>Paquete de seguridad de Kerberos

El paquete [*de seguridad de*](../secgloss/s-gly.md) Kerberos se basa en el protocolo de [*autenticación Kerberos*](../secgloss/k-gly.md).

Si el protocolo Kerberos se usa para autenticar una conexión de cliente/servidor, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) genera un mensaje GSSAPI que incluye un mensaje KRB AP REQ del \_ \_ cliente. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) genera a continuación un mensaje GSSAPI que incluye un mensaje KRB \_ AP REP desde el \_ servidor.

Para obtener información general sobre los pasos que tienen lugar en segundo plano en la implementación de un protocolo Kerberos, vea [Microsoft Kerberos](microsoft-kerberos.md).

Todos los servicios distribuidos usan SSPI para acceder al protocolo Kerberos. Una lista parcial de las formas en que se usa el protocolo Kerberos para la autenticación incluye:

-   Servicios de cola de impresión
-   Acceso remoto a archivos CIFS/SMB
-   [*Consultas LDAP*](../secgloss/l-gly.md) a la Active Directory
-   Administración y referencias del sistema de archivos distribuido
-   Autenticación de la entidad de seguridad de host a host de IPsec
-   Solicitudes de reserva para la calidad de servicio de red
-   Autenticación de intranet para Internet Information Services
-   Administración remota de servidores o estaciones de trabajo mediante RPC autenticado
-   [*Solicitudes de certificado a*](../secgloss/c-gly.md) Servicios de certificados para usuarios y equipos de dominio

## <a name="ntlm-security-package"></a>Paquete de seguridad NTLM

El paquete de seguridad NTLM se basa en el protocolo de autenticación NTLM.

 

 
