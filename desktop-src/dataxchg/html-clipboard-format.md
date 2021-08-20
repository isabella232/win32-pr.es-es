---
title: Formato del Portapapeles HTML
description: En esta sección se describe el formato del Portapapeles HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Interfaz de usuario,clipboard
- portapapeles, cortar datos
- clipboard,copying data
- clipboard, pegar datos
- clipboard,formats
- portapapeles, formato HTML
- portapapeles, cortar texto HTML
- portapapeles, pegar texto HTML
- CF_HTML formato del Portapapeles
- clipboard,CF_HTML format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafeb80c790ac511b3ffcd750ea4fbfafceeb7fb919842bb12a696b9655ab6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811662"
---
# <a name="html-clipboard-format"></a>Formato del Portapapeles HTML

Los requisitos para transferir texto HTML mediante el Portapapeles difieren en función del escenario. En este artículo se trata de cortar y pegar fragmentos de un documento HTML. Puede haber requisitos para transferir documentos HTML completos a través del Portapapeles. sin embargo, este artículo está controlado por un requisito para transferir fragmentos de texto HTML seleccionado. Por lo tanto, un método que requería que todo el documento HTML se copiara en el Portapapeles se ve como demasiado pesado.

El formato del Portapapeles CF HTML permite almacenar un fragmento de texto HTML sin formato y su contexto en el \_ Portapapeles como ASCII. Esto permite que una aplicación examine el contexto del fragmento HTML, que consta de todas las etiquetas circundantes anteriores, para que las etiquetas circundantes del fragmento HTML se puedan observar con sus atributos. Aunque las aplicaciones deciden cómo interpretar estos fragmentos, aquí se incluyen algunas directrices básicas basadas en implementaciones de IE4/MSHTML.

El nombre oficial del Portapapeles (la cadena usada por RegisterClipboardFormat) es Html Format.

-   [Descripción](#description)
-   [Escenarios](#scenarios)

## <a name="description"></a>Descripción

CF HTML es un formato de texto completo (para ser, entre otras cosas, en el lenguaje HTML y usa UTF-8) e incluye , un opcional y, dentro del \_ `description` `context` contexto, `fragment` .

A continuación se muestra un ejemplo de un Portapapeles:


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



La descripción incluye el número de versión del Portapapeles y los desplazamientos, lo que indica dónde comienzan y terminan el contexto y el fragmento. La descripción es una lista de palabras clave de texto ASCII (min/no es significativo) seguidas de una cadena y separadas por dos puntos (:).

**Versión:** número de versión de vv del Portapapeles. La versión inicial es la 0.9.

**StartHTML:** bytecount desde el principio del Portapapeles hasta el inicio del contexto, o -1 si no hay contexto.

**EndHTML:** bytecount desde el principio del Portapapeles hasta el final del contexto, o -1 si no hay contexto.

**StartFragment:** bytecount desde el principio del Portapapeles hasta el inicio del fragmento.

**EndFragment:** bytecount desde el principio del Portapapeles hasta el final del fragmento.

**StartSelection:** bytecount desde el principio del Portapapeles hasta el inicio de la selección.

**EndSelection:** bytecount desde el principio del Portapapeles hasta el final de la selección.

Las palabras clave StartSelection y EndSelection son opcionales y deben omitirse si no desea que la aplicación genere esta información.

Más adelante se podría agregar otra información de este tipo, ya que el código HTML se inicia en StartHTMLoffset. Por ejemplo, se podrían agregar varios pares de StartFragment/EndFragment más adelante para admitir la selección no continua de fragmentos.

Para mayor comodidad de los programas que generan los recuentos de bytes, los recuentos de bytes se pueden dejar con ceros. Por ejemplo, los programas que generan los recuentos de bytes podrían afectar arbitrariamente a diez (10) ceros a cada palabra clave (StartHTML: 0000000000) y, después, cuando se conoce el recuento de bytes de StartHTML exacto (por ejemplo, 71), el programa puede reemplazar el número adecuado de ceros por el número de bytes (StartHTML: 0000000071).

El único juego de caracteres admitido por el Portapapeles es Unicode en su codificación UTF-8. Dado que los primeros caracteres de UTF-8 y ASCII coinciden, la descripción siempre es ASCII, pero los bytes del contexto (a partir de StartHTML) podrían usar cualquier otro carácter codificado en UTF-8.

El final de las líneas en el encabezado de formato del Portapapeles podría ser CR, CR/LF o LF.

El fragmento contiene HTML puro y válido que representa el área que el usuario ha seleccionado (por ejemplo, copiar). Contiene el texto seleccionado, además de las etiquetas de apertura y los atributos de cualquier elemento que tenga una etiqueta final dentro del texto seleccionado, y las etiquetas finales al final del fragmento para cualquier etiqueta de inicio incluida. Esta es toda la información necesaria para pegar básicamente un fragmento HTML.

El fragmento debe ir precedido y seguido de los comentarios HTML <!--StartFragment--> y <!--EndFragment--> (no se permite espacio entre el !-- y el texto) para indicar cómodamente dónde comienza y termina el fragmento. Por lo tanto, el inicio y el final del fragmento se indican por la presencia de estos comentarios y por los recuentos de bytes StartFragment y EndFragment en la descripción. Se espera que las herramientas produzcan esta información. Esta redundancia se ha introducido para poder encontrar rápidamente el inicio del fragmento (a partir del recuento de bytes) y marcar la posición del fragmento directamente en el árbol HTML.

La selección indica dentro del fragmento el área HTML exacta que el usuario ha seleccionado (por ejemplo, copiar). Esto agrega más información al fragmento indicando el texto seleccionado exacto, sin las etiquetas de apertura y las etiquetas finales que se han agregado para asegurarse de que el fragmento tiene el formato HTML correcto.

La selección es opcional, ya que se incluye suficiente información en el fragmento para pegar básicamente. Si no se almacena la selección, StartSelection y EndSelection no se almacenan en el encabezado .

El contexto es un documento HTML completo y válido. Este artículo contiene el fragmento y todas las etiquetas circundantes anteriores (etiquetas inicial y final; estas etiquetas circundantes anteriores representan todos los nodos primarios del fragmento, hasta el nodo HTML). El artículo también contiene el head completo y permite incluir los elementos BASE y TITLE, por ejemplo, para que se pueda obtener esta información adicional. Una aplicación que copia un fragmento de HTML en el Portapapeles puede optar por crear un elemento BASE para incluirlo en el contexto si este elemento aún no está presente para que se puedan resolver las direcciones URL parciales del fragmento.

El contexto es opcional, ya que se incluye suficiente información en el fragmento para que se lleve a cabo la pega básica de un fragmento HTML. Si no se almacena el contexto, solo se almacena el fragmento y StartHTML=EndHTML=-1.

## <a name="scenarios"></a>Escenarios

En los escenarios siguientes se describe cómo el editor HTML de IE4/MSHTML controla el corte y pegado de HTML; Otras aplicaciones pueden o no seguir estos escenarios. El formato del Portapapeles que se describe aquí está pensado para permitir la flexibilidad de cómo una aplicación elige funcionar. (Estos escenarios muestran solo html bueno, es decir, sin etiquetas superpuestas).

1.  Fragmento simple de HTML.
    -   -   Texto HTML:

            <BODY>This is normal <B>This is bold </B>This is bold italic This is italic (Esto es cursiva en <I> <B> </B>negrita).</I></BODY>

        -   Aparece como:

            This is normal **This is bold** This is bold italic This is italic (Esto es cursiva en negrita). Esto es *** cursiva*  

        -   El texto entre se \* \* selecciona y se copia en el Portapapeles:

            This is normal **This is** \* \* **bold** This is bold italic This is italic (Esto es cursiva en *** negrita).* Esto \* \* *es cursiva*   

        -   Esto es lo que estará en el Portapapeles (tenga en cuenta que esta es la interpretación de IE4/MSHTML):

            Versión:0.9

            StartHTML:71

            EndHTML:160

            StartFragment:130

            EndFragment:150

            **StartSelection:130**

            **EndSelection:150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>negrita</B><I><B>Esta es cursiva en negrita.</B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   En este escenario, solo la etiqueta BODY y la etiqueta HTML aparecen en el contexto cuando precede al fragmento seleccionado. Tenga en cuenta que las etiquetas de inicio y las etiquetas finales se incluyen en el contexto. La selección, delimitada por StartSelection y EndSelection, se muestra en negrita.

2.  Fragmento de una tabla en HTML.
    -   -   Texto HTML:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Elemento 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE></BODY>

        -   Aparece como: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Elemento 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE><! \[ Cdata\[\]\]>
        -   Los elementos Item 6, Item7, Item 10 y Item 11 de la tabla se seleccionan como un bloque y se copian en el Portapapeles.
        -   Esto es lo que estará en el Portapapeles (tenga en cuenta que esta es la interpretación de IE4/MSHTML):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Item 6 </TD> <TD> Item 7 </TD> </TR> <TR> <TD> Item 10 </TD> <TD> Item 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  Pegar un fragmento de una lista ordenada en texto sin formato.
    -   -   Texto HTML:

            <BODY><OL TYPE = a><LI>Elemento 1<LI>Item 2<LI>Item 3<LI>Elemento 4<LI>Elemento 5<LI>Elemento 6</OL></BODY>

        -   Aparece como:
            1.  Elemento 1
            2.  Item 2
            3.  Item 3
            4.  Elemento 4
            5.  Elemento 5
            6.  Elemento 6
        -   El usuario selecciona y copia los elementos del 3 al 5 en el Portapapeles. El siguiente código HTML está en el Portapapeles:

            <DOCTYPE...><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Elemento <LI> 3, elemento <LI> 4, elemento 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            La selección, delimitada por StartSelection y EndSelection, se muestra en negrita.

        -   Si este fragmento se pega ahora en un documento vacío, se creará el siguiente código HTML:

            <BODY><OL TYPE = a><LI>Item 3<LI>Elemento 4<LI>Elemento 5</OL></BODY>

        -   Aparece como:
            1.  Item 3
            2.  Elemento 4
            3.  Elemento 5

4.  Pegar una región parcialmente seleccionada.
    -   -   Texto HTML:

            <P> IE4/MSHTML es un editor WYSIWYG que admite :<UL><LI>Cortar<LI>Copiar<LI>Pegar</UL><P>Esta es una herramienta excelente.

        -   Aparece como:IE4/MSHTML es un editor WYSIWYG que admite :
            -   -   Cortar
                -   Copiar
                -   Pegar

        -   El usuario selecciona desde "WYSIWYG" hasta "Cop". El siguiente código HTML está en el Portapapeles:

            <DOCTYPE...><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, que admite**

            **<UL><LI>Cut <LI> Cop**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   El usuario selecciona entre "opy" hasta "Great".

            El siguiente código HTML está en el Portapapeles:

            <DOCTYPE...><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **opy <LI> Paste This is a </UL> <P> Great**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            La selección, delimitada por StartSelection y EndSelection, se muestra en negrita.

 

 




