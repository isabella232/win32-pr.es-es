---
title: Cookies HTTP
description: Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704977"
---
# <a name="http-cookies"></a>Cookies HTTP

Las cookies HTTP proporcionan al servidor un mecanismo para almacenar y recuperar información de estado en el sistema de la aplicación cliente. Este mecanismo permite a las aplicaciones basadas en Web almacenar información sobre los elementos seleccionados, las preferencias del usuario, la información de registro y otra información que se puede recuperar más adelante.

## <a name="cookie-related-headers"></a>Encabezados de Cookie-Related

Hay dos encabezados, Set-Cookie y cookie, que están relacionados con las cookies. El servidor envía el encabezado Set-Cookie como respuesta a una solicitud HTTP, que se usa para crear una cookie en el sistema del usuario. La aplicación cliente incluye el encabezado de la cookie con una solicitud HTTP enviada a un servidor, si hay una cookie que tenga un dominio y una ruta de acceso coincidentes.

### <a name="set-cookie-header"></a>Encabezado Set-Cookie

El encabezado de respuesta Set-Cookie utiliza el formato siguiente:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

 = En el encabezado de respuesta Set-Cookie se deben incluir una o varias secuencias de cadenas (separadas por punto y coma) que sigan el *valor* del nombre del patrón. El servidor puede utilizar estas secuencias de cadenas para almacenar datos en el sistema del cliente.

La fecha de expiración se establece mediante el formato Expires =*Date*, donde *Date* es la fecha de expiración en la hora del meridiano de Greenwich (GMT). Si no se establece la fecha de expiración, la cookie expira una vez finalizada la sesión de Internet. De lo contrario, la cookie se conserva en la memoria caché hasta la fecha de expiración. La fecha debe tener el formato siguiente:

*día*, *DD* - *MMM* - *AAAA* *HH*:*mm*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*DIARIAMENTE*
</dt> <dd>

El día de la semana (sol, Lun, mar, Mié, Jue, Vie, SAT).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*DD*
</dt> <dd>

Día del mes (por ejemplo, 01 para el primer día del mes).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*MMM*
</dt> <dd>

La abreviatura de tres letras para el mes (Jan, Feb, mar, Apr, mayo, Jun, Jul, ago, Sep, Oct, Nov, DEC).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*AAA*
</dt> <dd>

Año.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

El valor de hora en hora militar (22 sería de 10:00 P.M., por ejemplo).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*MM*
</dt> <dd>

Valor del minuto.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*SS*
</dt> <dd>

Segundo valor.

</dd> </dl>

Especificar el nombre de dominio, con el patrón domain =*\_ nombre de dominio*, es opcional para las cookies persistentes y se usa para indicar el final del dominio para el que la cookie es válida. Se rechazan las cookies de sesión que especifican un dominio. Si el nombre de dominio especificado finaliza con la solicitud, la cookie intenta coincidir con la ruta de acceso para determinar si se debe enviar la cookie. Por ejemplo, si el nombre de dominio final es. microsoft.com, las solicitudes a home.microsoft.com y support.microsoft.com se comprueban para ver si el patrón especificado coincide con la solicitud. El nombre de dominio debe tener al menos dos o tres períodos para evitar que las cookies se establezcan para los finales de nombres de dominio ampliamente utilizados, como. com,. edu y co.jp. Los nombres de dominio permitidos serían similares a. microsoft.com,. someschool.edu y. someserver.co.jp. Solo los hosts dentro del dominio especificado pueden establecer una cookie para un dominio.

La configuración de la ruta de acceso, mediante la ruta de acceso del patrón =*some \_*, es opcional y se puede usar para especificar un subconjunto de las direcciones URL para las que la cookie es válida. Si se especifica una ruta de acceso, la cookie se considera válida para las solicitudes que coinciden con dicha ruta de acceso. Por ejemplo, si la ruta de acceso especificada es/example, las solicitudes con las rutas de acceso/examplecode y/example/code.htm coincidirán. Si no se especifica ninguna ruta de acceso, se supone que la ruta de acceso es la ruta de acceso del recurso asociado al encabezado Set-Cookie.

La cookie también se puede marcar como segura, lo que especifica que la cookie solo se puede enviar a servidores https.

Por último, una cookie se puede marcar como HttpOnly (los atributos no distinguen mayúsculas de minúsculas) para indicar que la cookie no admite scripts y no debe revelarse a la aplicación cliente por motivos de seguridad. Dentro de Windows Internet, esto significa que no se puede recuperar la cookie a través de la función **InternetGetCookie** .

### <a name="cookie-header"></a>Encabezado de cookie

El encabezado de la cookie se incluye con todas las solicitudes HTTP que tienen una cookie cuyo dominio y ruta de acceso coinciden con la solicitud. El encabezado de la cookie tiene el siguiente formato:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Una o varias secuencias de cadenas, utilizando el valor de *nombre* de formato = , contienen la información que se estableció en la cookie.

## <a name="generating-cookies"></a>Generar cookies

Existen tres métodos para generar cookies para Microsoft Internet Explorer: usar Microsoft JScript, usar las funciones de WinINet y usar un script CGI. Todos los métodos deben establecer la información que se incluye en el encabezado de Set-Cookie.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Generar una cookie mediante el modelo de objetos DHTML

Con el modelo de objetos de HTML dinámico (DHTML), las cookies se pueden establecer mediante una llamada a la propiedad **Cookie** del objeto de documento, tal y como se muestra en el ejemplo siguiente.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Generar una cookie mediante las funciones WinInet

Las aplicaciones pueden crear cookies mediante la función [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) . Para obtener más información, consulte [configuración de una cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Generación de una cookie mediante un script CGI

Las cookies se generan mediante la inclusión de un encabezado Set-Cookie como parte de un script CGI incluido en la respuesta HTTP a una solicitud.

El ejemplo siguiente es un script CGI que incluye un encabezado Set-Cookie mediante Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 