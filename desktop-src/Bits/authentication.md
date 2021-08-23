---
title: Autenticación (BITS)
description: BITS admite la autenticación básica, la autenticación de Passport y varios esquemas de autenticación de desafío/respuesta.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 9cb3d50f6689ed28889c68388969c1cb7d06ea912bc5d5ed4384f45a4e740f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021293"
---
# <a name="authentication-bits"></a>Autenticación (BITS)

BITS admite la autenticación básica, la autenticación de Passport y varios esquemas de autenticación de desafío/respuesta. Si el servidor o proxy requiere autenticación de usuario, use la función [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar las credenciales del usuario. BITS usa [CryptoAPI para](/windows/desktop/SecCrypto/cryptography-portal) proteger las credenciales.

Para establecer las credenciales para la autenticación básica, use [**la función SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar el nombre de usuario y la contraseña. Solo debe usar la autenticación básica con sitios https:// sitios web seguros protegidos. De lo contrario, el nombre de usuario y la contraseña serán visibles para los usuarios. 

Es posible insertar el nombre de usuario y la contraseña en la dirección URL. Esto no se considera una buena práctica de seguridad y está en desuso en RFC 3986 (sección 3.2.1).

Para [la autenticación](/windows/desktop/WinHttp/passport-authentication-in-winhttp) de Passport, BITS solo admite credenciales explícitas, no credenciales implícitas asociadas a la cuenta.

Para la autenticación de desafío/respuesta, BITS suplanta al usuario y usa [Snego](../com/snego.md) para determinar qué autenticación de desafío/respuesta usar, como NTLM o el protocolo Kerberos. Para obtener una lista de los esquemas de desafío y respuesta que admite BITS, vea [**BG \_ AUTH \_ SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

Los trabajos de BITS pueden producir un error si el directorio virtual del servidor tiene habilitada la autenticación anónima y otro esquema de autenticación, y si las ACL protegen el directorio virtual o descargan archivos. Por ejemplo, se produce un error en un trabajo con "acceso denegado" si el directorio virtual tiene habilitada la autenticación anónima e integrada y el archivo contiene una ACL que solo permite a Ben leer el archivo. Esto se debe a que el directorio virtual permite el acceso anónimo, por lo que IIS no autentica explícitamente a Ben (las credenciales de Ben no se usan para acceder al archivo y se deniega el acceso).

## <a name="using-implicit-credentials"></a>Uso de credenciales implícitas

Para usar las credenciales implícitas (de inicio de sesión) del usuario para la autenticación NTLM o Kerberos, llame al método [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) y establezca los miembros **UserName** y **Password** de la estructura [**BG BASIC \_ \_ CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) en **NULL.** Si especifica credenciales implícitas para un proxy, BITS también usará las credenciales implícitas para la autenticación de servidor a menos que especifique credenciales de servidor explícitas.

Para obtener información adicional sobre los servicios, vea [Cuentas de servicio y BITS.](service-accounts-and-bits.md)

También puede cambiar el valor del Registro **LMCompatibilityLevel** **o UseLMCompat.** sin embargo, solo debe cambiar estos valores si tiene una aplicación existente que no se puede cambiar para llamar al [**método SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)

BITS usará credenciales implícitas para la autenticación si el valor del Registro **LMCompatibilityLevel** es dos o superior y no ha llamado al [**método SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) La ruta de acceso completa al valor del Registro **LMCompatibilityLevel** es **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LmCompatibilityLevel**.

Tenga en cuenta que cambiar el valor del Registro **LMCompatibilityLevel** puede afectar a otras aplicaciones y servicios que se ejecutan en el equipo. Para obtener más información sobre el uso del valor del Registro **LMCompatibilityLevel,** vea [KB147706](https://support.microsoft.com/kb/147706).

Si establecer el valor del Registro **LMCompatibilityLevel** es un problema, puede crear el valor del Registro **UseLMCompat** en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS**. El valor del Registro es DWORD. En la tabla siguiente se enumeran los valores posibles **para UseLMCompat**:

|Value|Descripción|
|-|-|
| 0     | BITS enviará credenciales implícitas cada vez que el servidor solicite credenciales NTLM o Kerberos.                                                                                           |
| 1     | BITS enviará credenciales implícitas solo si el valor del Registro **LMCompatibilityLevel** del equipo cliente es mayor o igual que 2.<br/>     |
| 2     | BITS enviará credenciales implícitas solo si la aplicación llamó al [**método SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)<br/> |

BITS usará un valor predeterminado de "2" para el valor del Registro **UseLMCompat** si el valor del Registro no existe.

## <a name="using-certificates-for-clientserver-authentication"></a>Uso de certificados para la autenticación de cliente/servidor

En la comunicación segura entre cliente y servidor, los clientes y servidores pueden usar certificados digitales para autenticarse mutuamente entre sí. BITS admite automáticamente la autenticación de servidor basada en certificados para transportes HTTP seguros. Para proporcionar BITS al certificado de cliente necesario para la autenticación mutua, llame al método [**IBackgroundCopyJobHttpOptions::SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o [**IBackgroundCopyJobHttpOptions::SetClientCertificateByName.**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)

Cuando un sitio web acepta pero no requiere un certificado de cliente SSL y el trabajo de BITS no especifica un certificado de cliente, se producirá un error en el trabajo con **ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED** (0x80072f0c).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Cómo controlar escenarios de proxy autenticados que requieren una configuración específica del usuario

Si usa BITS en un entorno que requiere autenticación de proxy mientras se ejecuta como una cuenta sin credenciales NTLM o Kerberos utilizables en el dominio de red del equipo, debe realizar pasos adicionales para autenticarse correctamente mediante las credenciales de otra cuenta de usuario que tenga credenciales en el dominio. Este es un escenario típico cuando el código BITS se ejecuta como un servicio del sistema como LocalService, NetworkService o LocalSystem, ya que esas cuentas no tienen credenciales NTLM o Kerberos utilizables.

La lógica de detección de proxy usada en BITS hace lo siguiente cuando se establece un token auxiliar de red (BG \_ TOKEN \_ NETWORK):

-   Si se llamó a [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG JOB PROXY USAGE \_ \_ \_ \_ PRECONFIG**, lea la configuración del proxy de IE local mediante la suplantación del contexto del token del propietario del trabajo a través de [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). A partir Windows 10, versión 1809 (10.0; Compilación 17763), la identidad del token auxiliar se usa para este paso.
-   Si se llamó a [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG PROXY USAGE \_ \_ \_ AUTODETECT** o si la configuración de IE del caso **BG JOB PROXY USAGE \_ \_ \_ \_ PRECONFIG** especifica la detección automática o una dirección URL de configuración automática, realice la detección de proxy automático o el Protocolo de detección automática de proxy web (WPAD), mediante la suplantación del token auxiliar a través de [**WinHttpGetProxyForUrl.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)

Después de eso, la suplantación del token auxiliar se usa para la autenticación de servidor o proxy en todo el proceso.

A partir Windows 10, versión 1809 (10.0; Compilación 17763), se simplifica el escenario de proxy autenticado con credenciales específicas del usuario.

1.  Llame al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del trabajo bits con **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* establecido en **NULL,** *Password* establecido en **NULL** y *Target* establecido en **BG \_ AUTH TARGET \_ \_ PROXY.** Esto hace que las credenciales implícitas de la cuenta de usuario se usen para la autenticación NTLM y Kerberos con el proxy y el servidor.
2.  Llame [**a IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG JOB PROXY USAGE \_ \_ \_ \_ PRECONFIG**.
3.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Suplante la cuenta de usuario que usa para las credenciales NTLM/Kerberos.
5.  Llame [**a SetHelperToken.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
6. Llame [**a SetHelperTokenFlags con**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) BG TOKEN **\_ \_ NETWORK.**
7. Revierta la suplantación.
8. Continuar con la configuración del trabajo.
9. Llame [**a Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) en el trabajo.

Antes Windows 10, versión 1809 (10.0; Compilación 17763), la identidad de usuario correcta (la identidad del token auxiliar) se usa para la detección de proxy basado en red (WPAD) y para la autenticación de proxy, pero la detección real de la configuración de proxy local (IE) siempre se realiza mediante el token del propietario del trabajo, incluso cuando se configura un token auxiliar. Para evitar esta deficiencia, puede seguir estos pasos.

1.  Suplante la cuenta de usuario que usa para las credenciales NTLM/Kerberos.
2.  Recupere la configuración del proxy de IE de la cuenta de usuario mediante una [**llamada a WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).
3.  Revierta la suplantación.
4.  Llame al método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del trabajo bits con **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* establecido en **NULL,** *Password* establecido en **NULL** y *Target* establecido en **BG \_ AUTH TARGET \_ \_ PROXY.** Esto hace que las credenciales implícitas de la cuenta de usuario se usen para la autenticación NTLM y Kerberos con el proxy y el servidor.
5.  Si el paso 2 produjo una configuración de proxy específica del usuario (es decir, *lpszProxy* o *lpszProxyBypass* no son **NULL),** establezca la configuración del trabajo correspondiente manualmente, mediante [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la opción **BG JOB PROXY USAGE \_ \_ \_ \_ OVERRIDE.**
6.  Si el paso 2 no produjo ninguna configuración de proxy específica del usuario, llame a [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG JOB USAGE \_ \_ \_ PRECONFIG**.
7.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Vuelva a suplantar la cuenta de usuario.
9.  Llame [**a SetHelperToken.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
10. Llame [**a SetHelperTokenFlags con**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) BG TOKEN **\_ \_ NETWORK.**
11. Revierta la suplantación.
12. Continuar con la configuración del trabajo.
13. Llame [**a Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) en el trabajo.
