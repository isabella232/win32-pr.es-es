---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) admiten por completo el uso del lado cliente del Protocolo de autenticación de Microsoft Passport. En este tema se proporciona información general sobre las transacciones implicadas en la autenticación de Passport y cómo controlarlas.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Autenticación de Passport en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8fc00217c7c14fbd4635fab68398d2056c1ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496889"
---
# <a name="passport-authentication-in-winhttp"></a>Autenticación de Passport en WinHTTP

Los servicios HTTP de Microsoft Windows (WinHTTP) admiten por completo el uso del lado cliente del Protocolo de autenticación de Microsoft Passport. En este tema se proporciona información general sobre las transacciones implicadas en la autenticación de Passport y cómo controlarlas.

> [!Note]  
> En WinHTTP 5,1, la autenticación de Passport está deshabilitada de forma predeterminada.

 

## <a name="passport-14"></a>Passport 1,4

Passport es un componente básico de los servicios de bloques de creación de Microsoft .NET. Permite a las empresas desarrollar y ofrecer servicios Web distribuidos a través de una amplia gama de aplicaciones y permite a sus miembros usar un nombre de inicio de sesión y una contraseña en todos los sitios web participantes.

WinHTTP proporciona compatibilidad con la plataforma para Microsoft Passport 1,4 mediante la implementación del protocolo del lado cliente para la autenticación de Passport 1,4. Libera a las aplicaciones de los detalles de la interacción con la infraestructura de Passport y los nombres de usuario y contraseñas almacenados en Windows XP. Esta abstracción hace que el uso de Passport no sea diferente de la perspectiva de un desarrollador que el uso de esquemas de autenticación tradicionales como Basic o Digest.

**Windows XP:** La clave del registro **HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings de \\ Passport \\ NumRegistrationRuns** identifica el número de veces que se muestra el Asistente de autenticación de Passport cuando se requiere la autenticación de Passport. Si el valor de esta clave se establece en un número mayor que 5, no se muestra el asistente.

En las secciones siguientes se describen las transacciones implicadas en la autenticación de Passport desde el punto de vista de una aplicación cliente. Para el desarrollo de pasaporte del lado servidor, consulte la documentación de Passport SDK.

-   [Solicitud inicial](#initial-request)
-   [Servidor de inicio de sesión de Passport](#passport-login-server)
-   [Solicitud autenticada](#authenticated-request)

### <a name="initial-request"></a>Solicitud inicial

Cuando un cliente solicita un recurso en un servidor que requiere autenticación de Passport, el servidor comprueba la solicitud de presencia de [*vales*](glossary.md). Si se envía un *vale* válido con la solicitud, el servidor responde con el recurso solicitado. Si el *vale* no existe en el cliente, el servidor responde con un código de estado 302. La respuesta incluye el encabezado Challenge, "WWW-Authenticate: Passport 1.4". Los clientes que no utilizan Passport pueden seguir el redireccionamiento al servidor de inicio de sesión de Passport. Normalmente, los clientes más avanzados se pongan en contacto con el nexo de Passport para determinar la ubicación del servidor de inicio de sesión de Passport.

> [!Note]  
> El centro de la red Microsoft Passport es el *nexo* de Passport, que facilita la sincronización de sitios de participantes de Passport para garantizar que cada sitio tiene los detalles más recientes sobre la configuración de red y otros problemas. Cada componente de Passport (Administrador de Passport, servidores de inicio de sesión, servidores de actualización, etc.) se comunica periódicamente con el nexo para recuperar la información que necesita para localizar y comunicarse correctamente con los demás componentes de la red de Passport. Esta información se recupera como un documento XML denominado documento de configuración de componentes o CCD.

 

La siguiente imagen muestra la solicitud inicial a una afiliada de Passport.

![imagen muestra la solicitud inicial a una afiliada de Passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Servidor de inicio de sesión de Passport

Un servidor de inicio de sesión de Passport administra todas las solicitudes de [*vales*](glossary.md) de cualquier recurso de una *entidad de dominio* de Passport. Antes de poder autenticar una solicitud mediante Passport, la aplicación cliente debe ponerse en contacto con el servidor de inicio de sesión para obtener los *vales* adecuados.

Cuando un cliente solicita [*vales*](glossary.md) de un servidor de inicio de sesión de Passport, el servidor de inicio de sesión responde normalmente con un código de estado 401 para indicar que se deben proporcionar las credenciales del usuario. Cuando se proporcionan estas credenciales, el servidor de inicio de sesión responde con los *vales* necesarios para tener acceso al recurso especificado en el servidor que contiene el recurso solicitado originalmente. El servidor de inicio de sesión también puede redirigir el cliente a otro servidor que pueda proporcionar el recurso solicitado.

![la imagen muestra una solicitud de vale de cliente a un servidor de inicio de sesión de Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Solicitud autenticada

Cuando el cliente tiene los [*vales*](glossary.md) que corresponden a un servidor determinado, dichos *vales* se incluyen con todas las solicitudes a ese servidor. Si los *vales* no se han modificado desde que se recuperaron del servidor de inicio de sesión de Passport y los *vales* son válidos para el servidor de recursos, el servidor de recursos envía una respuesta que incluye el recurso y las cookies solicitados que indican que el usuario se autentica para futuras solicitudes.

Las cookies adicionales de la respuesta están pensadas para acelerar el proceso de autenticación. Las solicitudes adicionales en la misma sesión para los recursos de los servidores de la misma entidad de dominio de Passport incluyen estas cookies adicionales. No es necesario que las credenciales se envíen al servidor de inicio de sesión de nuevo hasta que expiren las cookies.

![imagen muestra una solicitud autenticada al servidor de inicio de sesión de Passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Usar Passport en WinHTTP

La autenticación de Passport en WinHTTP es muy similar a otros esquemas de autenticación. Vea [autenticación en WinHTTP](authentication-in-winhttp.md) para obtener información general sobre la autenticación en winhttp.

En WinHTTP 5,1, la autenticación de Passport está deshabilitada de forma predeterminada y debe habilitarse explícitamente con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) antes de su uso.

WinHTTP controla muchos de los detalles de la transacción internamente para la autenticación de Passport. Durante la solicitud inicial, el servidor responde con un código de estado 302 cuando se necesita autenticación. El código de estado 302 indica realmente una redirección y forma parte del protocolo Passport para la compatibilidad con versiones anteriores. WinHTTP oculta el código de estado 302 y se pone en contacto con el nexo de Passport y, después, con el servidor de inicio de sesión. La aplicación WinHTTP recibe una notificación del código de estado 401 enviado por el servidor de inicio de sesión para solicitar las credenciales de usuario. Sin embargo, en la aplicación aparece como si el estado 401 fuera del servidor desde el que se solicitó el recurso. De esta manera, la aplicación WinHTTP no es consciente de las interacciones con otros servidores y puede controlar la autenticación de Passport con el mismo código que controla otros esquemas de autenticación.

Normalmente, una aplicación WinHTTP responde a un código de estado 401 proporcionando credenciales de autenticación. Cuando las credenciales se suministran con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**SetCredentials**](iwinhttprequest-setcredentials.md) para la autenticación de Passport, las credenciales se envían realmente al servidor de inicio de sesión, no al servidor indicado en la solicitud.

Sin embargo, cuando se responde a un código de estado 407, una aplicación WinHTTP debe usar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar credenciales de proxy, en lugar de [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Dado que **WinHttpSetOption** es una manera menos segura de proporcionar credenciales, normalmente se debe evitar.

Una vez recuperados, los [*vales*](glossary.md) se administran internamente y se envían automáticamente a los servidores correspondientes en solicitudes futuras.

> [!Note]  
> WinHTTP le permite deshabilitar el redireccionamiento automático mediante una llamada a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para la [**\_ opción WinHTTP \_ deshabilitar \_**](option-flags.md) la marca de características y especificar un valor de [**WinHTTP \_ Disable \_ redirects**](option-flags.md). Deshabilitar el redireccionamiento no interfiere con la redirección que WinHTTP controla internamente para las transacciones de Passport.

 

WinHTTP puede completar correctamente la autenticación de Passport aunque una aplicación deshabilite la redirección automática. Sin embargo, una vez completada la autenticación de Passport, se debe producir una redirección implícita desde la dirección URL del servidor de inicio de sesión de Passport de nuevo a la dirección URL original. Una respuesta HTTP 302 no desencadena esta redirección, pero está implícita en el protocolo Passport.

WinHTTP controla este redireccionamiento implícito de forma especial. Si una aplicación ha deshabilitado el redireccionamiento automático, WinHTTP requiere que la aplicación proporcione "permiso" de WinHTTP para redirigir automáticamente en este caso especial.

Para hacer que WinHTTP redirija a la dirección URL original después de la autenticación, la aplicación debe registrar una función de devolución de llamada mediante [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback). A continuación, WinHTTP puede notificar a la aplicación con una \_ devolución de llamada de REdirección de estado de devolución de llamada \_ de WinHTTP \_ , que permite a la aplicación cancelar la redirección. No es necesario que una aplicación proporcione ninguna funcionalidad en la función de devolución de llamada. el registro de la devolución de llamada es suficiente para permitir que WinHTTP siga esta redirección de casos especiales.

El mensaje de error de \_ Inicio de sesión de WinHTTP \_ \_ se genera si la aplicación no establece una función de devolución de llamada.

### <a name="passport-cobranding"></a>Personalización de marca de Passport

A diferencia de los esquemas de autenticación tradicionales que admite WinHTTP, Passport puede tener una [*copersonalización*](glossary.md)ampliada. Al recibir un código de estado 401 que indica un desafío, una aplicación puede recuperar el texto y el gráfico de *copersonalización de marca* . Recupere una dirección URL para el gráfico de *copersonalización* mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la \_ opción WinHTTP \_ \_ dirección URL de copersonalización de marca de Passport \_ . Recupere el texto de la *Personalización de marca* mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la opción de WinHTTP de \_ \_ \_ copersonalización de marca de Passport \_ . Estos elementos se pueden usar para personalizar un cuadro de diálogo de recopilación de credenciales.

### <a name="stored-user-names-and-passwords"></a>Nombres de usuarios y contraseñas almacenados

Windows XP presentó el concepto de nombres de usuario y contraseñas almacenados. Si las credenciales de Passport de un usuario se guardan mediante el **Asistente para registro de Passport** o el **cuadro de diálogo credencial** estándar, se guardan en los nombres de usuario y contraseñas almacenados. Al usar WinHTTP en Windows XP o versiones posteriores, WinHTTP usa automáticamente las credenciales en los nombres de usuario y contraseñas almacenados si no se establecen explícitamente las credenciales. Esto es similar a la compatibilidad con las credenciales de inicio de sesión predeterminadas para NTLM/Kerberos. Sin embargo, el uso de las credenciales predeterminadas de Passport no está sujeto a la configuración de la Directiva de inicio de sesión automático.

### <a name="disabling-passport-authentication"></a>Deshabilitación de la autenticación de Passport

Es posible que algunas aplicaciones requieran la posibilidad de deshabilitar la autenticación de Passport. Por ejemplo, cuando una filial de Passport responde con el código de estado 302 inicial, podría ser preferible seguir el redireccionamiento indicado y representar la página de autenticación de Passport HTML en lugar de permitir que WinHTTP controle la autenticación internamente. La autenticación de Passport está deshabilitada en WinHTTP mediante una llamada a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la \_ opción WinHTTP \_ configure \_ Passport \_ auth y pasando el valor WinHTTP \_ Disable \_ Passport \_ auth. Posteriormente, se puede volver a habilitar con WINHTTP \_ habilitar \_ Passport \_ auth.

No se puede deshabilitar la autenticación de Passport cuando se usa el objeto [**WinHttpRequest**](winhttprequest.md) .

Como se indicó anteriormente en esta sección, la autenticación de Passport está deshabilitada de forma predeterminada en WinHTTP 5,1 y debe habilitarse explícitamente con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) antes de su uso.

## <a name="passport-configuration-overrides-used-for-testing"></a>Invalidaciones de configuración de Passport utilizadas para las pruebas

WinHTTP se basa en la información de configuración que descarga del servidor de Passport Nexus para admitir la autenticación de Passport 1,4. De forma predeterminada, este servidor seguro (SSL) es nexus.passport.com y el recurso de configuración es RDR/pprdr. asp, que se conoce como la configuración de Passport "activa". El formato de la información es un encabezado HTTP personalizado "PassportURLs", seguido de pares de atributo-valor delimitados por comas.

Por ejemplo, " https://nexus.passport.com/rdr/pprdr.asp " devuelve la siguiente información de configuración:

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

Las partes que son relevantes para WinHTTP son DARealm, DALogin y ConfigVersion. Por motivos de rendimiento, se almacenan en memoria caché mientras dure una sesión de WinHTTP. Estos tres valores pueden ser invalidados por aplicaciones que son necesarias para trabajar con otra infraestructura de Passport distinta de la configuración de producción "activa" cambiando la configuración del registro adecuada en

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

Si LoginServerUrl está presente en el registro, WinHTTP no se pone en contacto con el servidor de Nexus para obtener otros valores de configuración. En este caso, LoginServerRealm y ConfigVersion también se deben establecer en el registro para corregir los valores.

Una aplicación puede, con fines de prueba, ser necesaria para descargar la configuración de Passport de un servidor de Nexus privado. Esto puede hacerse invalidando dos valores del registro en

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación en WinHTTP](authentication-in-winhttp.md)
</dt> </dl>

 

 



