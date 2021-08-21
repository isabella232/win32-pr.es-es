---
description: Microsoft Windows HTTP Services (WinHTTP) admite totalmente el uso del lado cliente del protocolo Microsoft Passport autenticación. En este tema se proporciona información general sobre las transacciones implicadas en la autenticación de Passport y cómo controlarlas.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Autenticación de Passport en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d6aff7f8924c307d4e21efb77bc57ebae2469e50361b57d12dce5b348555e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114321"
---
# <a name="passport-authentication-in-winhttp"></a>Autenticación de Passport en WinHTTP

Microsoft Windows HTTP Services (WinHTTP) admite totalmente el uso del lado cliente del protocolo Microsoft Passport autenticación. En este tema se proporciona información general sobre las transacciones implicadas en la autenticación de Passport y cómo controlarlas.

> [!Note]  
> En WinHTTP 5.1, la autenticación de Passport está deshabilitada de forma predeterminada.

 

## <a name="passport-14"></a>Passport 1.4

Passport es un componente básico de la Microsoft .NET servicios de bloque de creación. Permite a las empresas desarrollar y ofrecer servicios web distribuidos en una amplia gama de aplicaciones y permite a sus miembros usar un nombre de inicio de sesión y una contraseña en todos los sitios web participantes.

WinHTTP proporciona compatibilidad de plataforma Microsoft Passport 1.4 mediante la implementación del protocolo del lado cliente para la autenticación de Passport 1.4. Libera a las aplicaciones de los detalles de la interacción con la infraestructura de Passport y los nombres de usuario y contraseñas almacenados en Windows XP. Esta abstracción hace que el uso de Passport no sea diferente de la perspectiva de un desarrollador que el uso de esquemas de autenticación tradicionales como Basic o Digest.

**Windows XP:** La clave del Registro **HKCU \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet Configuración Passport \\ \\ \\ NumRegistrationRuns** identifica el número de veces que se muestra el Asistente para autenticación de Passport cuando se requiere la autenticación PassPort. Si el valor de esta clave se establece en un número mayor que 5, no se muestra el asistente.

En las secciones siguientes se describen las transacciones implicadas en la autenticación de Passport desde el punto de vista de una aplicación cliente. Para el desarrollo de Passport en el lado servidor, consulte información general sobre la documentación del SDK de Passport.

-   [Solicitud inicial](#initial-request)
-   [Servidor de inicio de sesión de Passport](#passport-login-server)
-   [Solicitud autenticada](#authenticated-request)

### <a name="initial-request"></a>Solicitud inicial

Cuando un cliente solicita un recurso en un servidor que requiere autenticación passport, el servidor comprueba la solicitud de presencia de [*vales*](glossary.md). Si se envía *un vale* válido con la solicitud, el servidor responde con el recurso solicitado. Si el *vale* no existe en el cliente, el servidor responde con un código de estado 302. La respuesta incluye el encabezado del desafío, "WWW-Authenticate: Passport1.4". Los clientes que no usan Passport pueden seguir el redireccionamiento al servidor de inicio de sesión de Passport. Los clientes más avanzados suelen ponerse en contacto con passport nexus para determinar la ubicación del servidor de inicio de sesión de Passport.

> [!Note]  
> La red de Microsoft Passport principal es Passport *Nexus,* que facilita la sincronización de los sitios de participantes de Passport para garantizar que cada sitio tiene los detalles más recientes sobre la configuración de red y otros problemas. Cada componente de Passport (Passport Manager, servidores de inicio de sesión, servidores de actualización, entre otros) se comunica periódicamente con Nexus para recuperar la información que necesita para localizar y comunicarse correctamente con los demás componentes de la red de Passport. Esta información se recupera como un documento XML denominado documento de configuración de componentes o CCD.

 

En la imagen siguiente se muestra la solicitud inicial a una afiliada de Passport.

![Imagen que muestra la solicitud inicial a una afiliada de Passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Servidor de inicio de sesión de Passport

Un servidor de inicio de sesión de Passport controla todas las solicitudes [*de vales*](glossary.md) para cualquier recurso de una entidad de *dominio de* Passport. Para poder autenticar una solicitud mediante Passport, la aplicación cliente debe ponerse en contacto con el servidor de inicio de sesión para obtener los vales *adecuados.*

Cuando un cliente solicita [*vales*](glossary.md) a un servidor de inicio de sesión de Passport, el servidor de inicio de sesión suele responder con un código de estado 401 para indicar que se deben proporcionar credenciales de usuario. Cuando se proporcionan estas credenciales, el  servidor de inicio de sesión responde con los vales necesarios para acceder al recurso especificado en el servidor que contiene el recurso solicitado originalmente. El servidor de inicio de sesión también puede redirigir el cliente a otro servidor que pueda proporcionar el recurso solicitado.

![Image muestra una solicitud de vale de cliente a un servidor de inicio de sesión de Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Solicitud autenticada

Cuando el cliente tiene los [*vales*](glossary.md) que corresponden a un servidor determinado, esos *vales* se incluyen con todas las solicitudes a ese servidor. Si  los vales no se han modificado desde que se  recuperaron del servidor de inicio de sesión de Passport y los vales son válidos para el servidor de recursos, el servidor de recursos envía una respuesta que incluye el recurso solicitado y las cookies que indican que el usuario está autenticado para solicitudes futuras.

Las cookies adicionales de la respuesta están diseñadas para acelerar el proceso de autenticación. Las solicitudes adicionales en la misma sesión para los recursos de los servidores de la misma autoridad de dominio de Passport incluyen estas cookies adicionales. No es necesario volver a enviar las credenciales al servidor de inicio de sesión hasta que expiren las cookies.

![image muestra una solicitud autenticada al servidor de inicio de sesión de Passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Uso de Passport en WinHTTP

La autenticación de Passport en WinHTTP es muy similar a otros esquemas de autenticación. Consulte [Autenticación en WinHTTP para](authentication-in-winhttp.md) obtener información general sobre la autenticación en WinHTTP.

En WinHTTP 5.1, la autenticación de Passport está deshabilitada de forma predeterminada y debe habilitarse explícitamente [**con WinHttpSetOption antes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) de su uso.

WinHTTP controla muchos de los detalles de la transacción internamente para la autenticación de Passport. Durante la solicitud inicial, el servidor responde con un código de estado 302 cuando es necesaria la autenticación. El código de estado 302 realmente indica un redireccionamiento y forma parte del protocolo Passport para la compatibilidad con versiones anteriores. WinHTTP oculta el código de estado 302 y se pone en contacto con Passport Nexus y, a continuación, con el servidor de inicio de sesión. Se notifica a la aplicación WinHTTP el código de estado 401 enviado por el servidor de inicio de sesión para solicitar las credenciales de usuario. Sin embargo, para la aplicación, parece como si el estado 401 se origina en el servidor desde el que se solicitó el recurso. De esta manera, la aplicación WinHTTP no es consciente de las interacciones con otros servidores y puede controlar la autenticación de Passport con el mismo código que controla otros esquemas de autenticación.

Normalmente, una aplicación WinHTTP responde a un código de estado 401 mediante el suministro de credenciales de autenticación. Cuando se proporcionan credenciales con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**SetCredentials**](iwinhttprequest-setcredentials.md) para la autenticación de Passport, las credenciales se envían realmente al servidor de inicio de sesión, no al servidor indicado en la solicitud.

Sin embargo, al responder a un código de estado 407, una aplicación WinHTTP debe usar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar credenciales de proxy, en lugar [**de WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Dado **que WinHttpSetOption** es una manera menos segura de proporcionar credenciales, normalmente se debe evitar.

Una vez recuperados, [*los vales*](glossary.md) se administran internamente y se envían automáticamente a los servidores aplicables en solicitudes futuras.

> [!Note]  
> WinHTTP permite deshabilitar el redireccionamiento automático llamando a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para la marca [**WINHTTP \_ OPTION DISABLE \_ \_ FEATURE**](option-flags.md) y especificando un valor de [**WINHTTP DISABLE \_ \_ REDIRECTS**](option-flags.md). Deshabilitar el redireccionamiento no interfiere con el redireccionamiento que WinHTTP controla internamente para las transacciones de Passport.

 

WinHTTP puede completar correctamente la autenticación de Passport aunque una aplicación deshabilite el redireccionamiento automático. Sin embargo, una vez completada la autenticación de Passport, debe producirse un redireccionamiento implícito desde la dirección URL del servidor de inicio de sesión de Passport a la dirección URL original. Esta redirección no se desencadena mediante una respuesta HTTP 302, pero está implícita en el protocolo Passport.

WinHTTP controla este redireccionamiento implícito especialmente. Si una aplicación ha deshabilitado el redireccionamiento automático, WinHTTP requiere que la aplicación dé "permiso" a WinHTTP para redirigir automáticamente en este caso especial.

Para que WinHTTP vuelva a redirigirse a la dirección URL original después de la autenticación, la aplicación debe registrar una función de devolución de llamada [**mediante WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback). A continuación, WinHTTP puede notificar a la aplicación con una devolución de llamada CALLBACK STATUS REDIRECT de WINHTTP, lo que permite a la aplicación \_ \_ cancelar la \_ redirección. Una aplicación no necesita proporcionar ninguna funcionalidad en la función de devolución de llamada; El registro de la devolución de llamada es suficiente para permitir que WinHTTP siga este redireccionamiento de caso especial.

El mensaje ERROR WINHTTP LOGIN FAILURE se genera si la aplicación no establece una función de devolución \_ \_ de \_ llamada.

### <a name="passport-cobranding"></a>Passport Cobranding

A diferencia de los esquemas de autenticación tradicionales admitidos por WinHTTP, Passport se puede [*cambiar ampliamente a la marca*](glossary.md). Tras recibir un código de estado 401 que indica un desafío, una aplicación puede recuperar el gráfico *y* el texto de marca comarca. Recupere una dirección URL para el gráfico de marca *comarca* mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la marca DE DIRECCIÓN \_ URL DE \_ COBRANDING DE WINHTTP OPTION \_ \_ PASSPORT. Recupere el *texto de marca* comarca mediante una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con la marca DE TEXTO WINHTTP \_ OPTION PASSPORT \_ \_ COBRANDING. \_ Estos elementos se pueden usar para personalizar un cuadro de diálogo de recopilación de credenciales.

### <a name="stored-user-names-and-passwords"></a>Nombres de usuarios y contraseñas almacenados

Windows XP introdujo el concepto de nombres de usuario y contraseñas almacenados. Si las credenciales de Passport de un usuario se guardan mediante el Asistente para registro de **Passport** o el cuadro de diálogo de credenciales **estándar,** se guarda en los nombres de usuario y contraseñas almacenados. Cuando se usa WinHTTP en Windows XP o posterior, WinHTTP usa automáticamente las credenciales de los nombres de usuario y contraseñas almacenados si las credenciales no se establecen explícitamente. Esto es similar a la compatibilidad de las credenciales de inicio de sesión predeterminadas para NTLM/Kerberos. Sin embargo, el uso de credenciales predeterminadas de Passport no está sujeto a la configuración de la directiva de inicio de sesión automático.

### <a name="disabling-passport-authentication"></a>Deshabilitación de la autenticación de Passport

Algunas aplicaciones pueden requerir la capacidad de deshabilitar la autenticación de Passport. Por ejemplo, cuando una afiliada de Passport responde con el código de estado 302 inicial, puede ser preferible seguir el redireccionamiento indicado y representar la página de autenticación de HTML Passport en lugar de permitir que WinHTTP controle la autenticación internamente. La autenticación de Passport está deshabilitada en WinHTTP llamando a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción CONFIGURE PASSPORT AUTH de WINHTTP OPTION y pasando el valor \_ \_ \_ \_ WINHTTP \_ DISABLE PASSPORT \_ \_ AUTH. Más adelante se puede volver a habilitar con WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH.

La autenticación de Passport no se puede deshabilitar cuando se usa [**el objeto WinHttpRequest.**](winhttprequest.md)

Como se indicó anteriormente en esta sección, la autenticación de Passport está deshabilitada de forma predeterminada en WinHTTP 5.1 y debe habilitarse explícitamente [**con WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) antes de su uso.

## <a name="passport-configuration-overrides-used-for-testing"></a>Invalidaciones de configuración de Passport usadas para las pruebas

WinHTTP se basa en la información de configuración que descarga del servidor passport nexus para admitir la autenticación de Passport 1.4. De forma predeterminada, este servidor seguro (SSL) es nexus.passport.com y el recurso de configuración es rdr/pprdr.asp, que se conoce como la configuración "activa" de Passport. El formato de la información es un encabezado HTTP personalizado "PassportURLs", seguido de pares de atributo-valor delimitados por comas.

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

Las partes que son relevantes para WinHTTP son DARealm, DALogin y ConfigVersion. Por motivos de rendimiento, se almacenan en caché durante la vigencia de una sesión WinHTTP. Estos tres valores se pueden reemplazar por las aplicaciones necesarias para trabajar con otra infraestructura de Passport que no sea la configuración de producción "en directo" cambiando la configuración del Registro adecuada en

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

Si LoginServerUrl está presente en el Registro, WinHTTP no se pondrá en contacto con el servidor Nexus para obtener otros valores de configuración. En este caso, LoginServerRealm y ConfigVersion también se deben establecer a través del Registro para corregir los valores.

Una aplicación puede, con fines de prueba, ser necesaria para descargar la configuración de Passport desde un servidor Nexus privado. Esto se puede hacer reemplazando dos valores del Registro en

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

 

 



