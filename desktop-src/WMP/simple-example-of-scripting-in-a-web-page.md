---
title: Ejemplo sencillo de scripting en una página web
description: Ejemplo sencillo de scripting en una página web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Control ActiveX de Windows Media Player, ejemplo de scripting
- Control ActiveX móvil de Windows Media Player, ejemplo de scripting
- Control ActiveX, ejemplo de scripting
- incrustación, páginas web
- Incrustación de páginas web, ejemplo de scripting
- ejemplo de scripting para la inserción de páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105704825"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>Ejemplo sencillo de scripting en una página web

Puede incrustar fácilmente el control Media Player de Windows en un archivo HTML mediante cualquier lenguaje de scripting que reconozca el explorador. En el siguiente ejemplo simple se usa Microsoft JScript para crear una página que reproducirá un archivo al hacer clic en un botón y detener la reproducción del archivo al hacer clic en otro botón.

Puede incrustar el control ActiveX de Windows Media Player en una página web mediante los cuatro pasos siguientes:

1.  Cree la Página Web.
2.  Agregue la etiqueta de objeto.
3.  Agregue una interfaz de usuario. En este caso, dos botones.
4.  Agregue algunas líneas de código para responder cuando el usuario haga clic en uno de los botones que ha creado.

## <a name="creating-the-web-page"></a>Creación de la página web

El primer paso es crear una página web HTML válida. El código siguiente es el mínimo necesario para crear una página HTML en blanco pero válida:


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>Agregar la etiqueta de objeto

Una vez que haya creado una página web, debe agregar una etiqueta de objeto. Esto identifica el control ActiveX en el explorador y configura las definiciones iniciales. Debe colocar la etiqueta de objeto en el cuerpo del código. Si lo coloca en el cuerpo, se mostrará la interfaz de usuario predeterminada de Windows Media Player. Si desea crear su propia interfaz de usuario, establezca los atributos height y width en 0 (cero). También puede establecer el *reproductor*. la propiedad **uiMode** en "invisible" cuando se desea ocultar el control, pero aún se reserva espacio para él en la página. El código siguiente se recomienda cuando se proporciona una interfaz de usuario personalizada:


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



Se requieren los siguientes atributos de etiqueta de objeto:

id

Nombre que usarán otras partes del código para identificar y usar el control ActiveX. Puede elegir cualquier nombre que desee, siempre que sea un nombre que no esté siendo utilizado por HTML, extensiones HTML o el lenguaje de scripting que esté usando. En este ejemplo, se usa el nombre "Player", pero también puede llamarlo "Replay" u otra cosa. Simplemente seleccione un nombre que sea único para esa página web.

CLASSID

Un número hexadecimal muy grande que es único para el control. Solo un control tiene este número y es el control ActiveX de Windows Media Player. Para evitar errores tipográficos, puede copiar y pegar este número de la documentación. Las versiones del control de Windows Media Player anteriores a la versión 7,0 tenían un CLASSID diferente.

## <a name="adding-a-user-interface"></a>Agregar una interfaz de usuario

HTML permite una gran cantidad de elementos de la interfaz de usuario, lo que permite al usuario interactuar con la página web haciendo clic, presionando las teclas y otras acciones del usuario. Agregar algunos botones de entrada es la forma más fácil de proporcionar una interfaz de usuario rápida. En el código siguiente se crean dos botones que pueden responder al usuario. Al hacer clic en un botón, se inicia la reproducción del flujo multimedia y el otro botón lo detiene:


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



El nombre del botón se usa para identificar el botón en el código; el valor es la etiqueta que aparecerá en el botón y el atributo OnClick identifica a qué parte del código de script se llamará cuando se haga clic en el botón.

## <a name="adding-scripting-code"></a>Agregar código de scripting

El código de script agrega interactividad a la página. El código de scripting puede responder a eventos, llamar a métodos y cambiar las propiedades de tiempo de ejecución. Los scripts extendidos se incluyen en un conjunto de etiquetas de SCRIPT. La etiqueta de SCRIPT indica al explorador que el código de scripting es e identifica el lenguaje de scripting. Si no identifica un idioma, el idioma predeterminado será Microsoft JScript.

Es aconsejable escribir el script en etiquetas de Comentario HTML para que los exploradores que no admiten el scripting no representen el código como texto. Coloque la etiqueta de SCRIPT en cualquier parte del cuerpo del archivo HTML e inserte el código rodeado de comentarios dentro de las etiquetas de SCRIPT de apertura y cierre.

El siguiente ejemplo de código de Microsoft JScript llama al control Media Player de Windows y realiza una acción adecuada en respuesta al clic de botón correspondiente.


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



Se llama a la función de ejemplo, StartMeUp, cuando se hace clic en el botón de reproducción marcado de reproducción y se llama a la función ShutMeDown cuando se hace clic en el botón detener.

El código dentro de StartMeUp usa la propiedad URL para definir una ruta de acceso a los elementos multimedia. Los elementos multimedia comenzarán a reproducirse inmediatamente.

El código ShutMeDown llama al método **Stop** del objeto **Controls** . Tenga en cuenta que se llama al objeto **Controls** mediante la propiedad **Controls** del objeto **Player** , que tiene el valor de ID de "Player".

En el código siguiente se muestra un ejemplo completo.


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



Tenga en cuenta que debe proporcionar una dirección URL válida a un nombre de archivo válido en la propiedad URL. En este caso, se supone que el archivo Laure. WMA está en el mismo directorio que el archivo HTML.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Media Player de Windows en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




