---
title: Formato del portapapeles HTML
description: En esta sección se describe el formato del portapapeles HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interfaz de usuario de Windows, Portapapeles
- portapapeles, cortar datos
- portapapeles, copiar datos
- portapapeles, pegar datos
- portapapeles, formatos
- portapapeles, formato HTML
- portapapeles, cortar texto HTML
- portapapeles, pegar texto HTML
- CF_HTML formato del portapapeles
- portapapeles, formato de CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075895"
---
# <a name="html-clipboard-format"></a>Formato del portapapeles HTML

Los requisitos para transferir texto HTML por medio del portapapeles difieren en función del escenario. Este artículo está relacionado con la corte y pegado de fragmentos de un documento HTML. Puede haber requisitos para transferir documentos HTML completos a través del portapapeles; sin embargo, este artículo está controlado por un requisito para transferir fragmentos del texto HTML seleccionado. Como tal, un método que requiera copiar el documento HTML completo en el portapapeles se considera demasiado pesado.

El \_ formato del portapapeles HTML de CF permite que un fragmento de texto HTML sin formato y su contexto se almacenen en el portapapeles como ASCII. Esto permite que una aplicación examine el contexto del fragmento HTML, que consta de todas las etiquetas adyacentes, para que las etiquetas circundantes del fragmento HTML se puedan anotar con sus atributos. Aunque es el caso de las aplicaciones decidir cómo interpretar estos fragmentos, algunas instrucciones básicas se incluyen aquí en función de las implementaciones de IE4/MSHTML.

El nombre oficial del portapapeles (la cadena usada por RegisterClipboardFormat) es el formato HTML.

-   [Descripción](#description)
-   [Escenarios](#scenarios)

## <a name="description"></a>Descripción

El \_ HTML de CF tiene un formato de texto completo (por ejemplo, entre otras cosas, en el espíritu HTML y usa UTF-8) e incluye un `description` , un opcional `context` y, dentro del contexto, `fragment` .

El siguiente es un ejemplo de un portapapeles:


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



La descripción incluye el número de versión y los desplazamientos del portapapeles, lo que indica dónde se inicia y finaliza el contexto y el fragmento. La descripción es una lista de palabras clave de texto ASCII (min/Mayús no es significativa) seguida de una cadena y separadas por dos puntos (:).

**Versión**: número de versión de VV del portapapeles. La versión inicial es 0,9.

**StartHTML**: byteCount desde el principio del Portapapeles hasta el inicio del contexto, o-1 si no hay ningún contexto.

**Entext: byteCount** desde el principio del Portapapeles hasta el final del contexto, o-1 si no hay contexto.

**StartFragment**: byteCount desde el principio del Portapapeles hasta el inicio del fragmento.

**EndFragment**: byteCount desde el principio del Portapapeles hasta el final del fragmento.

**StartSelection**: byteCount desde el principio del Portapapeles hasta el inicio de la selección.

**EndSelection**: byteCount desde el principio del Portapapeles hasta el final de la selección.

Las palabras clave StartSelection y EndSelection son opcionales y deben omitirse ambos si no desea que la aplicación genere esta información.

Otra información de este tipo podría agregarse aquí más adelante, ya que el código HTML se inicia en el StartHTMLoffset. Por ejemplo, se podrían agregar varios pares de StartFragment/EndFragment más adelante para admitir la selección no contigua de fragmentos.

Para la comodidad de los programas que generan el bytecounts, bytecounts podría quedar rellenado con ceros. Por ejemplo, los programas que generan el bytecounts podrían afectar arbitrariamente los diez (10) ceros a cada palabra clave (StartHTML: 0000000000) y, a continuación, cuando se conoce el byteCount exacto de StartHTML (por ejemplo, 71), el programa puede reemplazar el número de ceros adecuado por el byteCount (StartHTML: 0000000071).

El único juego de caracteres que admite el portapapeles es Unicode en su codificación UTF-8. Dado que los primeros caracteres de UTF-8 y ASCII coinciden, la descripción es siempre ASCII, pero los bytes del contexto (a partir de StartHTML) podrían usar cualquier otro carácter codificado en UTF-8.

El final de las líneas en el encabezado de formato del portapapeles podría ser CR o CR/LF o LF.

El fragmento contiene código HTML puro y válido que representa el área seleccionada por el usuario (para copiarla, por ejemplo). Contiene el texto seleccionado más las etiquetas de apertura y los atributos de cualquier elemento que tenga una etiqueta de cierre dentro del texto seleccionado y las etiquetas de cierre al final del fragmento para cualquier etiqueta de apertura incluida. Esta es toda la información necesaria para el pegado básico de un fragmento HTML.

El fragmento debe ir precedido y seguido de los comentarios HTML <!--StartFragment--> y <!--EndFragment--> (no se permite ningún espacio entre el!--y el texto) para indicar cómo se inicia y finaliza el fragmento. Por lo tanto, el inicio y el final del fragmento se indican mediante la presencia de estos comentarios y los recuentos de bytes StartFragment y EndFragment en la descripción. Se espera que las herramientas generen esta información. Esta redundancia se ha introducido para poder encontrar rápidamente el inicio del fragmento (desde el recuento de bytes) y marcar la posición del fragmento directamente en el árbol HTML.

La selección indica dentro del fragmento el área HTML exacta que el usuario ha seleccionado (para copiarlo, por ejemplo). Esto agrega más información al fragmento indicando el texto exacto seleccionado, sin las etiquetas de apertura y las etiquetas de cierre que se han agregado para asegurarse de que el fragmento es HTML con formato correcto.

La selección es opcional, ya que se incluye suficiente información en el fragmento para el pegado básico. Si no se almacena la selección, StartSelection y EndSelection no se almacenan en el encabezado.

El contexto es un documento HTML válido y completo. Este artículo contiene el fragmento y todas las etiquetas adyacentes anteriores (etiquetas de inicio y finalización; las etiquetas circundantes anteriores representan todos los nodos primarios del fragmento, hasta el nodo HTML). El artículo también contiene el encabezado completo y permite incluir los elementos BASE y título, por ejemplo, para que se pueda obtener esta información adicional. Una aplicación que copia un fragmento de HTML en el portapapeles puede optar por crear un elemento BASE para incluirlo en el contexto si este elemento no está ya presente para que se puedan resolver las direcciones URL parciales del fragmento.

El contexto es opcional, ya que se incluye suficiente información en el fragmento para que tenga lugar el pegado básico de un fragmento HTML. Si no se almacena el contexto, solo se almacena el fragmento y StartHTML = endhtml =-1.

## <a name="scenarios"></a>Escenarios

En los escenarios siguientes se describe cómo el editor HTML IE4/MSHTML controla el corte y pegado HTML. otras aplicaciones pueden o no seguir estos escenarios. El formato del portapapeles que se describe aquí está diseñado para permitir la flexibilidad en el modo en que una aplicación elige funcionar. (Estos escenarios muestran solo un buen código HTML, es decir, no hay etiquetas superpuestas).

1.  Fragmento simple de HTML.
    -   -   Texto HTML:

            <BODY>Esto es normal si se pone en <B>negrita </B>y está en negrita <I> <B>cursiva </B></I> .</BODY>

        -   Aparece como:

            Esto es normal si se pone en **negrita** y está en negrita    * **cursiva**   .

        -   El texto \* \* que se encuentra entre el se selecciona y se copia en el portapapeles:

            Esto **es normal si se pone** en \* \* **negrita** ,    *    \* \*  es decir, si está en cursiva.

        -   Esto es lo que se incluirá en el portapapeles (tenga en cuenta que se trata de la interpretación de IE4/MSHTML):

            Versión: 0.9

            StartHTML: 71

            DHTML: 160

            StartFragment: 130

            EndFragment: 150

            **StartSelection: 130**

            **EndSelection: 150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>Bold</B><I><B>es negrita cursiva</B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   En este escenario, solo la etiqueta de cuerpo y la etiqueta HTML aparecen en el contexto como precede al fragmento seleccionado. Tenga en cuenta que las etiquetas de inicio y las etiquetas de cierre se incluyen en el contexto. La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.

2.  Fragmento de una tabla en HTML.
    -   -   Texto HTML:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Elemento 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE></BODY>

        -   Aparece como: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Elemento 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE><. \[ CDATA\[\]\]>
        -   Los elementos item 6, Item7 (, Item 10 y Item 11 de la tabla se seleccionan como un bloque y se copian en el portapapeles.
        -   Esto es lo que se incluirá en el portapapeles (tenga en cuenta que se trata de la interpretación de IE4/MSHTML):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Elemento 6 elemento </TD> <TD> 7 elemento </TD> </TR> <TR> <TD> 10 </TD> <TD> elemento 11</TD></TR>**

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
        -   El usuario selecciona y copia los elementos 3 a 5 en el portapapeles. El siguiente código HTML está en el portapapeles:

            <DOCTYPE... ><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Elemento 3 elemento <LI> 4 <LI> elemento 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.

        -   Si este fragmento se pega ahora en un documento vacío, se creará el siguiente código HTML:

            <BODY><OL TYPE = a><LI>Item 3<LI>Elemento 4<LI>Elemento 5</OL></BODY>

        -   Aparecen como:
            1.  Item 3
            2.  Elemento 4
            3.  Elemento 5

4.  Pegar una región parcialmente seleccionada.
    -   -   Texto HTML:

            <P> IE4/MSHTML es un editor WYSIWYG que admite:<UL><LI>Cortar<LI>Copiar<LI>Pegar</UL><P>Esta es una herramienta excelente.

        -   Aparece como: IE4/MSHTML es un editor WYSIWYG que admite:
            -   -   Cortar
                -   Copiar
                -   Pegar

        -   El usuario selecciona "WYSIWYG" hasta "COP". El siguiente código HTML está en el portapapeles:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, que admite**

            **<UL><LI>Cortar <LI> COP**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   El usuario selecciona "opiar" hasta "excelente".

            El siguiente código HTML está en el portapapeles:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **copiar y <LI> pegar </UL> <P> esto es una excelente**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            La selección, como delimitada por StartSelection y EndSelection, se muestra en negrita.

 

 




