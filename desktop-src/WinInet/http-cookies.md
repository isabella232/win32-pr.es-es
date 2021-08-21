---
title: HTTP Cookies
description: Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113719"
---
# <a name="http-cookies"></a>HTTP Cookies

Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente. Este mecanismo permite a las aplicaciones basadas en web almacenar información sobre los elementos seleccionados, las preferencias del usuario, la información de registro y otra información que se puede recuperar más adelante.

## <a name="cookie-related-headers"></a>Cookie-Related encabezados

Hay dos encabezados, Set-Cookie y Cookie, que están relacionados con las cookies. El Set-Cookie envía el encabezado de la aplicación en respuesta a una solicitud HTTP, que se usa para crear una cookie en el sistema del usuario. La aplicación cliente incluye el encabezado Cookie con una solicitud HTTP enviada a un servidor, si hay una cookie que tiene un dominio y una ruta de acceso correspondientes.

### <a name="set-cookie-header"></a>Set-Cookie encabezado

El Set-Cookie de respuesta utiliza el formato siguiente:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Una o varias secuencias de cadena (separadas por punto y coma) que siguen el valor del nombre del patrón deben incluirse en el encabezado Set-Cookie =  respuesta. El servidor puede usar estas secuencias de cadenas para almacenar datos en el sistema del cliente.

La fecha de expiración se establece con el formato expires=*date*, donde *date* es la fecha de expiración en Greenwich Mean Time (GMT). Si no se establece la fecha de expiración, la cookie expira una vez que finaliza la sesión de Internet. De lo contrario, la cookie se conserva en la memoria caché hasta la fecha de expiración. La fecha debe usar el formato siguiente:

*DAY*, *DD* - *MMM* - *YYYY* *HH*:*MM*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*Día*
</dt> <dd>

El día de la semana (Dom, Mon, Mar, Mié, Jue, Viernes, Sábado).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*Dd*
</dt> <dd>

El día del mes (por ejemplo, 01 para el primer día del mes).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*Mmm*
</dt> <dd>

Abreviatura de tres letras del mes (enero, febrero, marzo, abril, mayo, junio, julio, agosto, sep, octubre, noviembre, dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*Aaaa*
</dt> <dd>

Año.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*Hh*
</dt> <dd>

El valor de hora en hora de las fuerzas (22 sería 10:00 p. m., por ejemplo).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*Mm*
</dt> <dd>

Valor del minuto.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*Ss*
</dt> <dd>

Segundo valor.

</dd> </dl>

La especificación del nombre de dominio, con el patrón domain= nombre de dominio , es opcional para las cookies persistentes y se usa para indicar el final del dominio para el que la cookie es válida.*\_* Se rechazan las cookies de sesión que especifican un dominio. Si el nombre de dominio especificado que finaliza coincide con la solicitud, la cookie intenta coincidir con la ruta de acceso para determinar si se debe enviar la cookie. Por ejemplo, si el nombre de dominio final es .microsoft.com, se comprobarán las solicitudes a home.microsoft.com y support.microsoft.com para ver si el patrón especificado coincide con la solicitud. El nombre de dominio debe tener al menos dos o tres períodos para evitar que se establezcan cookies para los finales de nombres de dominio ampliamente usados, como .com, .edu y co.jp. Los nombres de dominio permitidos serían similares a .microsoft.com, .someschool.edu y .someserver.co.jp. Solo los hosts del dominio especificado pueden establecer una cookie para un dominio.

Establecer la ruta de acceso, mediante la ruta de acceso del patrón = alguna ruta de acceso , es opcional y se puede usar para especificar un subconjunto de las direcciones URL para las que la cookie es válida.*\_* Si se especifica una ruta de acceso, la cookie se considera válida para las solicitudes que coincidan con esa ruta de acceso. Por ejemplo, si la ruta de acceso especificada es /example, las solicitudes con las rutas de acceso /examplecode y /example/code.htm coincidirían. Si no se especifica ninguna ruta de acceso, se supone que es la ruta de acceso del recurso asociado al Set-Cookie encabezado.

La cookie también se puede marcar como segura, lo que especifica que la cookie solo se puede enviar a servidores HTTPS.

Por último, una cookie se puede marcar como HttpOnly (los atributos no distinguen mayúsculas de minúsculas), para indicar que la cookie no es de script y no debe mostrarse a la aplicación cliente, por motivos de seguridad. En Windows Internet, esto significa que la cookie no se puede recuperar a través de la **función InternetGetCookie.**

### <a name="cookie-header"></a>Encabezado de cookie

El encabezado Cookie se incluye con cualquier solicitud HTTP que tenga una cookie cuyo dominio y ruta de acceso coincidan con la solicitud. El encabezado Cookie tiene el formato siguiente:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Una o varias secuencias de cadena, con el valor de *nombre de* formato , contienen la información que se = estableció en la cookie.

## <a name="generating-cookies"></a>Generación de cookies

Hay tres métodos para generar cookies para Microsoft Internet Explorer: usar Microsoft JScript, usar las funciones WinINet y usar un script CGI. Todos los métodos deben establecer la información que se incluye en el Set-Cookie encabezado.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Generar una cookie mediante el modelo de objetos DHTML

Con el modelo de objetos HTML dinámico (DHTML), las cookies se pueden establecer llamando a la propiedad **cookie** del objeto de documento, como se muestra en el ejemplo siguiente.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Generar una cookie mediante las funciones de WinInet

Las aplicaciones pueden crear cookies mediante la [**función InternetSetCookie.**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) Para obtener más información, vea [Establecer una cookie.](managing-cookies.md)

### <a name="generating-a-cookie-using-a-cgi-script"></a>Generar una cookie mediante un script CGI

Las cookies se generan mediante la inclusión Set-Cookie encabezado como parte de un script CGI incluido en la respuesta HTTP a una solicitud.

El ejemplo siguiente es un script CGI que incluye un encabezado Set-Cookie mediante Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 