---
title: Autenticación (BITS)
description: BITS admite la autenticación básica, la autenticación de Passport y varios esquemas de autenticación de desafío/respuesta.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 5d970956676a3348dd4b8c4b420e044bd4714775
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995832"
---
# <a name="authentication-bits"></a>Autenticación (BITS)

BITS admite la autenticación básica, la autenticación de Passport y varios esquemas de autenticación de desafío/respuesta. Si el servidor o proxy requiere autenticación de usuario, use la función [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar las credenciales del usuario. BITS usa [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) para proteger las credenciales.

Para establecer credenciales para la autenticación básica, use la función [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar el nombre de usuario y la contraseña. Solo debe usar la autenticación básica con sitios Web seguros protegidos mediante https://. de lo contrario, el nombre de usuario y la contraseña serán visibles para los usuarios. 

Es posible insertar el nombre de usuario y la contraseña en la dirección URL. Esto no se considera una buena práctica de seguridad y quedó en desuso en RFC 3986 (sección 3.2.1).

Para la autenticación de [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) , bits solo admite credenciales explícitas, no credenciales implícitas asociadas a la cuenta.

Para la autenticación de desafío/respuesta, BITS suplanta al usuario y usa [Snego](../com/snego.md) para determinar la autenticación de desafío/respuesta que se va a usar, como NTLM o el protocolo Kerberos. Para obtener una lista de esquemas de desafío/respuesta compatibles con BITS, consulte el [**\_ \_ esquema de autenticación de BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

Los trabajos de BITS pueden producir un error si el directorio virtual del servidor tiene autenticación anónima y otro esquema de autenticación habilitado y si las ACL protegen el directorio virtual o los archivos de descarga. Por ejemplo, se produce un error en un trabajo con "acceso denegado" si el directorio virtual tiene habilitada la autenticación anónima e integrada, y el archivo contiene una ACL que solo permite a Ben leer el archivo. Esto se debe a que el directorio virtual permite el acceso anónimo, por lo que IIS no autentica explícitamente Ben (las credenciales de Ben no se usan para tener acceso al archivo y se deniega el acceso).

## <a name="using-implicit-credentials"></a>Usar credenciales IMPLÍCITAS

Para usar las credenciales IMPLÍCITAS (inicio de sesión) del usuario para la autenticación NTLM o Kerberos, llame al método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) y establezca los miembros de **nombre de usuario** y **contraseña** de la estructura [**BG \_ Basic \_ Credentials**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) en **null**. Si especifica credenciales implícitas para un proxy, BITS también usará las credenciales implícitas para la autenticación de servidor a menos que especifique las credenciales de servidor explícitas.

Para obtener información adicional acerca de los servicios, consulte [cuentas de servicio y bits](service-accounts-and-bits.md).

También puede cambiar el valor del registro **LMCompatibilityLevel** o **UseLMCompat** ; sin embargo, solo debe cambiar estos valores si tiene una aplicación existente que no se puede cambiar para llamar al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .

BITS usará credenciales implícitas para la autenticación si el valor del registro **LMCompatibilityLevel** es dos o más, y no se ha llamado al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . La ruta de acceso completa al valor del registro **LMCompatibilityLevel** es **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **LSA** \\ **LMCompatibilityLevel**.

Tenga en cuenta que el cambio del valor del registro **LMCompatibilityLevel** puede afectar a otras aplicaciones y servicios que se ejecutan en el equipo. Para obtener más información acerca del uso del valor del registro **LMCompatibilityLevel** , vea [KB147706](https://support.microsoft.com/kb/147706).

Si establecer el valor del registro **LMCompatibilityLevel** es un problema, puede crear el valor del registro **UseLMCompat** en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **bits**. El valor del registro es un valor DWORD. En la tabla siguiente se enumeran los posibles valores para **UseLMCompat**:

|Value|Descripción|
|-|-|
| 0     | BITS enviará credenciales implícitas siempre que el servidor solicite las credenciales NTLM o Kerberos.                                                                                           |
| 1     | BITS enviará credenciales implícitas solo si el valor del registro **LMCompatibilityLevel** del equipo cliente es mayor o igual que 2.<br/>     |
| 2     | BITS enviará credenciales implícitas solo si la aplicación llamó al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .<br/> |

BITS usará un valor predeterminado de "2" para el valor del registro **UseLMCompat** si el valor del registro no existe.

## <a name="using-certificates-for-clientserver-authentication"></a>Uso de certificados para la autenticación de cliente/servidor

En la comunicación segura entre cliente y servidor, los clientes y servidores pueden usar certificados digitales para autenticarse mutuamente entre sí. BITS admite automáticamente la autenticación de servidor basada en certificados para transportes HTTP seguros. Para proporcionar BITS al certificado de cliente necesario para la autenticación mutua, llame al método [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByName**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) .

Cuando un sitio web acepta pero no requiere un certificado de cliente SSL y el trabajo de BITS no especifica un certificado de cliente, se producirá un error en el trabajo con el **error \_ WinHTTP \_ Client \_ auth \_ CERT \_** (0x80072f0c).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Cómo controlar los escenarios de proxy autenticados que requieren una configuración específica del usuario

Si usa BITS en un entorno que requiere autenticación de proxy mientras se ejecuta como una cuenta sin credenciales NTLM o Kerberos que se pueden usar en el dominio de red del equipo, debe realizar pasos adicionales para autenticarse correctamente mediante el uso de las credenciales de otra cuenta de usuario que tenga credenciales en el dominio. Se trata de un escenario típico en el que el código BITS se ejecuta como un servicio del sistema como LocalService, NetworkService o LocalSystem, ya que esas cuentas no tienen credenciales NTLM o Kerberos que se puedan usar.

La lógica de detección de proxy utilizada en BITS hace lo siguiente cuando se establece un token de aplicación auxiliar de red ( \_ red de tokens BG \_ ):

-   Si se llamó a [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la configuración de uso del proxy de trabajo de BG, lea configuración de proxy de IE local mediante la suplantación del contexto del token del propietario del trabajo a través de [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). **\_ \_ \_ \_** A partir de Windows 10, versión 1809 (10,0; Compilación 17763), se usa la identidad del token auxiliar para este paso.
-   Si se llamó a [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la detección automática del uso del proxy de BG o si la configuración de IE del caso de **\_ \_ \_ \_ preconfiguración de uso del proxy del trabajo de BG** especifica detección automática o una dirección URL de configuración automática, realice la detección de proxy automático o el protocolo de detección automática de proxy web (WPAD) mediante la suplantación de token de aplicación auxiliar mediante [**WinHttpGetProxyForUrl**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl). **\_ \_ \_**

Después de eso, la suplantación de tokens auxiliares se utiliza para la autenticación de servidor o proxy en todo.

A partir de Windows 10, versión 1809 (10,0; Compilación 17763), se simplifica el escenario de proxy autenticado con credenciales específicas del usuario.

1.  Llame al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del trabajo de bits con el **esquema de \_ autenticación BG \_ \_ Negotiate**, el *nombre de usuario* establecido en **null**, la *contraseña* establecida en **null** y el *destino* establecido en proxy de **\_ \_ destino \_ de autenticación BG**. Esto hace que se usen las credenciales implícitas de la cuenta de usuario para la autenticación NTLM y Kerberos con el proxy y el servidor.
2.  Llame a [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la configuración de uso del proxy de trabajo de **BG \_ \_ \_ \_**.
3.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Suplantar la cuenta de usuario que está usando para las credenciales de NTLM/Kerberos.
5.  Llame a [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
6. Llame a [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con la **\_ \_ red de tokens BG**.
7. Revertir la suplantación.
8. Continúe con la configuración del trabajo.
9. Llame a [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) en el trabajo.

Antes de Windows 10, versión 1809 (10,0; Compilación 17763), la identidad de usuario correcta (la identidad del token auxiliar) se usa para la detección de proxy basada en red (WPAD) y para la autenticación de proxy, pero la detección real de la configuración de proxy local (IE) siempre se realiza mediante el token del propietario del trabajo, incluso cuando se configura un token auxiliar. Para solucionar este defecto, puede seguir estos pasos.

1.  Suplantar la cuenta de usuario que está usando para las credenciales de NTLM/Kerberos.
2.  Recupere la configuración del proxy de IE de la cuenta de usuario mediante una llamada a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).
3.  Revertir la suplantación.
4.  Llame al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del trabajo de bits con el **esquema de \_ autenticación BG \_ \_ Negotiate**, el *nombre de usuario* establecido en **null**, la *contraseña* establecida en **null** y el *destino* establecido en proxy de **\_ \_ destino \_ de autenticación BG**. Esto hace que se usen las credenciales implícitas de la cuenta de usuario para la autenticación NTLM y Kerberos con el proxy y el servidor.
5.  Si el paso 2 produce una configuración de proxy específica del usuario (es decir, *lpszProxy* o *LpszProxyBypass* no son **null**), establezca la configuración de trabajo correspondiente manualmente, usando [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la configuración de **\_ \_ \_ \_ invalidación de uso del proxy del trabajo de BG** .
6.  Si el paso 2 no produjo ninguna configuración de proxy específica del usuario, llame a [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la **configuración de uso del trabajo de BG \_ \_ \_**.
7.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Vuelva a suplantar la cuenta de usuario.
9.  Llame a [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
10. Llame a [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con la **\_ \_ red de tokens BG**.
11. Revertir la suplantación.
12. Continúe con la configuración del trabajo.
13. Llame a [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) en el trabajo.
