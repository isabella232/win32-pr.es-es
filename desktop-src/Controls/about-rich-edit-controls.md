---
title: Acerca de los controles Rich Edit
description: En esta sección se presentan controles de edición enriquecidos.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742295358be32fa318334ceac7f89607adcbba12
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423995"
---
# <a name="about-rich-edit-controls"></a>Acerca de los controles Rich Edit

En esta sección se tratan los temas siguientes.

-   [Versiones de Rich Edit](#versions-of-rich-edit)
    -   [Edición enriquecte versión 1.0](#rich-edit-version-10)
    -   [Edición enriquecte versión 2.0](#rich-edit-version-20)
    -   [Edición enriquecte versión 3.0](#rich-edit-version-30)
    -   [Edición enriquecte versión 4.1](#rich-edit-version-41)
-   [Funcionalidad de edición de control no admitida](#unsupported-edit-control-functionality)
-   [Teclas de método abreviado rich edit](#rich-edit-shortcut-keys)
-   [Temas relacionados](#related-topics)

## <a name="versions-of-rich-edit"></a>Versiones de Rich Edit

La especificación original de los controles de edición enriquecciones es Microsoft Rich Edit 1.0; La especificación actual es Microsoft Rich Edit 4.1. Cada versión de edición enriquecida es un superconjunto del anterior, salvo que solo las compilaciones de Asia de Microsoft Rich Edit 1.0 tienen una opción de texto vertical. Antes de crear un control de edición enriquecido, debe llamar a la [**función LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para comprobar qué versión de Microsoft Rich Edit está instalada.

En la tabla siguiente se muestra qué archivo DLL se corresponde con la versión de Rich Edit. Tenga en cuenta que el nombre del archivo no cambió de la versión 2.0 a la versión 3.0. Esto permite actualizar la versión 2.0 a la versión 3.0 sin que se rompa el código existente.



| Edición enriquección de la versión | Archivo DLL          | Clase Window    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | RICHEDIT \_ (CLASE) |
| 2.0               | Riched20.dll | RICHEDIT \_ (CLASE) |
| 3.0               | Riched20.dll | RICHEDIT \_ (CLASE) |
| 4,1               | Msftedit.dll | MSFTEDIT \_ (CLASE) |



 

### <a name="rich-edit-version-10"></a>Edición enriquecte versión 1.0

Microsoft Rich Edit 1.0 incluye las siguientes características.



|    Característica   | Descripción   |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selección y entrada de texto                                                           | Principalmente la selección estándar (control de edición del sistema) y la entrada de texto. Compatibilidad con la barra de selección (la barra de selección es un área sin marca a la izquierda de cada párrafo que, al hacer clic en ella, selecciona la línea). Opciones de ajuste de palabras y selección automática de palabras. Selección de un solo clic, doble y triple clic. |
| Edición de ANSI (juego de caracteres de un solo byte (SBCS) y juego de caracteres multibyte (MBCS)) | Sin embargo, no hay ninguna edición Unicode.                                                                                                                                                                                                                                                     |
| Conjunto básico de propiedades de formato de caracteres/párrafos                             | Vea [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) y [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Propiedades de formato de caracteres                                                    | Nombre y tamaño de fuente, negrita, cursiva, subrayado sólido, tachado, protegido, vínculo, desplazamiento y color de texto.                                                                                                                                                                                   |
| Propiedades de formato de párrafo                                                    | Sangría inicial, sangría derecha, desplazamiento de línea posterior, viñeta, alineación (izquierda, centro, derecha) y pestañas.                                                                                                                                                                                    |
| Buscar hacia delante                                                                       | Incluye opciones que no tienen en cuenta mayúsculas y minúsculas y que coinciden con palabras enteras.                                                                                                                                                                                                                                   |
| Interfaz basada en mensajes                                                            | Casi un superconjunto del conjunto de mensajes de control de edición del sistema más dos interfaces, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) [**e IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                              |
| Objetos insertados                                                                   | Requiere colaboración de cliente basada [**en interfaces IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) [**e IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                          |
| Compatibilidad con el menú del botón derecho                                                          | Usa [**la interfaz IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                                                                                                      |
| Edición de arrastrar y colocar                                                              | Se admite la edición de arrastrar y colocar.                                                                                                                                                                                                                                                       |
| Notificaciones                                                                      | [**WM \_ Mensajes COMMAND**](/windows/desktop/menurc/wm-command) enviados al cliente más otros. Se trata de un superconjunto de notificaciones de control común.                                                                                                                                                 |
| Deshacer/rehacer de un solo nivel                                                             | Se comporta de forma similar al control de edición del sistema. Al seleccionar **Deshacer,** se invierte la última acción y, a continuación, esa acción se convierte en la **nueva acción Rehacer.**                                                                                                                                          |
| Texto vertical simple                                                               | (solo compilaciones de Asia).                                                                                                                                                                                                                                                                      |
| Compatibilidad con el Editor de métodos de entrada (IME)                                                  | (solo compilaciones de Asia).                                                                                                                                                                                                                                                                      |
| Edición de WYSIWYG mediante métricas de impresora                                              | Esta característica es necesaria para Microsoft WordPad, en particular.                                                                                                                                                                                                                              |
| Cortar, copiar, pegar, streamin/streamout                                                  | Con texto sin formato **(CF \_ TEXT)** o formato de texto enriquecido (RTF) con y sin objetos .                                                                                                                                                                                                        |
| Código base de C                                                                        | El código está escrito en C, que proporciona una base sólida y versátil.                                                                                                                                                                                                                |
| Diferentes compilaciones para distintos scripts                                             | Microsoft Rich Edit 1.0 aborda los problemas de localización con diferentes compilaciones.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Edición enriquecte versión 2.0

Microsoft Rich Edit 2.0 incorporó varias características adicionales, como la compatibilidad con idiomas Unicode y asiáticos, deshacer de varios niveles, interfaces del modelo de objetos componentes (COM) y numerosas mejoras en la interfaz de usuario.

Microsoft Rich Edit 2.0 incluye las siguientes características, además de las características proporcionadas por [Microsoft Rich Edit 1.0.](#rich-edit-version-10)



|    Característica                                           |    Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode facilita el trabajo de control del texto internacional. Sin embargo, se necesita esfuerzo para mantener la compatibilidad con documentos no Unicode existentes, es decir, la capacidad de convertir texto sin formato y enriquecido que no sea Unicode.                                                                                                                                                             |
| Soporte técnico internacional general                 | Algoritmo general de separación de líneas (extensión de reglas de Kinsoku), vinculación de fuentes simple, cambio de fuente de teclado.                                                                                                                                                                                                                                                                          |
| Soporte técnico asiático                                 | Se admiten los niveles 2 (cuadro de diálogo) y 3 (en línea) en los IME.                                                                                                                                                                                                                                                                                                                            |
| Buscar o buscar soporte técnico                     | Se admite la búsqueda hacia delante y hacia atrás.                                                                                                                                                                                                                                                                                                                                         |
| Compatibilidad bidireccional                         | Esto se incluye en Microsoft Rich Edit 2.1                                                                                                                                                                                                                                                                                                                                          |
| Deshacer varios niveles                               | Una arquitectura de deshacer extensible permite al cliente participar en el modelo deshacer en toda la aplicación.                                                                                                                                                                                                                                                                                         |
| Compatibilidad con el mouse de Magellan                        | Se trata del mouse con un rodillo para desplazarse.                                                                                                                                                                                                                                                                                                                                       |
| Compatibilidad con fuentes duales                             | El teclado puede cambiar automáticamente las fuentes cuando la fuente activa no es apropiada para el teclado actual, por ejemplo, los caracteres Kanji en Times New Roman.                                                                                                                                                                                                                            |
| Aplicación de fuente inteligente                              | La solicitud de cambio de fuente no aplica fuentes occidental a caracteres asiáticos.                                                                                                                                                                                                                                                                                                                |
| Pantalla mejorada                              | Se usa un mapa de bits fuera de la pantalla cuando se producen varias fuentes en la misma línea. Esto permite, por ejemplo, que la última letra de la palabra es cool no se desencapspede.                                                                                                                                                                                                                           |
| Compatibilidad con la transparencia                          | También en modo sin ventanas.                                                                                                                                                                                                                                                                                                                                                             |
| Colores de selección del sistema                       | Se usa para seleccionar texto.                                                                                                                                                                                                                                                                                                                                                             |
| Reconocimiento automático de direcciones URL                     | Puede comprobar si hay varios formatos de dirección URL (por ejemplo, http:)                                                                                                                                                                                                                                                                                                                           |
| Compatibilidad con la interfaz de usuario de edición de Microsoft Word          | Selección, semántica del teclado del cursor.                                                                                                                                                                                                                                                                                                                                                  |
| EOP estándar de Word                             | La marca de fin de párrafo (CR) también puede controlar el retorno de carro/avance de línea (CR/LF) (retorno de carro, avance de línea).                                                                                                                                                                                                                                                                       |
| Texto sin formato, así como funcionalidad de texto enriquecido | Formato de un solo carácter y formato de párrafo único.                                                                                                                                                                                                                                                                                                                                 |
| Controles de una sola línea y de varias líneas            | Truncar en el primer final del párrafo y sin ajuste de palabras.                                                                                                                                                                                                                                                                                                                                  |
| Teclas de aceleración                              | Se admiten las teclas de aceleración.                                                                                                                                                                                                                                                                                                                                                      |
| Estilo de ventana de contraseña                         | Los controles de edición de contraseñas se proporcionan a [**través de EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md) y [**EM \_ SETPASSWORDCHAR.**](em-setpasswordchar.md)                                                                                                                                                                                                                                 |
| Arquitectura escalable                         | Para reducir el tamaño de la instancia.                                                                                                                                                                                                                                                                                                                                                             |
| Operaciones e interfaces sin ventanas           | Esto se proporciona a través de [**las interfaces ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) [**e ITextServices.**](/windows/desktop/api/Textserv/nl-textserv-itextservices)                                                                                                                                                                                                                                                                   |
| Interfaces duales COM                           | Interfaces del Modelo de objetos de texto (TOM).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Se ha agregado el grosor de la fuente, el color de fondo, el identificador de configuración regional, el tipo de subrayado, el superíndice y el subíndice (además del desplazamiento), efecto deshabilitado. Solo para el redondeo RTF, se ha agregado una cantidad de espacio entre letras, un tamaño de twip por encima del cual se va a emparejar el carácter kern, el tipo de texto animado, varios efectos: sombra o contorno de fuente, todos los límites, los límites pequeños, ocultos, relieves, la impresión y la revisión. |
| PARAFORMAT2                                   | Se ha agregado espacio antes y después de y espaciado de línea de Word. Solo para el redondeo RTF, se ha agregado el peso o estilo de sombreado, la numeración de inicio,estilo/tabulación, espacio de borde/ancho/lados, alineación de tabulación/líderes, diversos efectos de párrafo de Word: párrafo RTL, keep, keep-next, page-break-before, no-line-number, no--la-- --hyphenate, side-by-side.                                         |
| Más redondeo RTF                        | Todas las propiedades FormatFont y FormatParagraph de Word.                                                                                                                                                                                                                                                                                                                           |
| Estabilidad y estabilización del código              | Ejemplos: validación de parámetros y objetos, invariables de función, protección de reenentrancy, estabilización de objetos.                                                                                                                                                                                                                                                                             |
| Infraestructura de pruebas seguras                 | Incluir pruebas de regresiones exhaustivas.                                                                                                                                                                                                                                                                                                                                               |
| rendimiento mejorado.                          | Un espacio de trabajo más pequeño, tiempos de carga y visualización más rápidos, y así sucesivamente.                                                                                                                                                                                                                                                                                                                     |
| Base de código de C++                                 | El código está escrito en C++, que proporciona una base sólida sobre la que compilar Microsoft Rich Edit 3.0.                                                                                                                                                                                                                                                                             |



 

Con algunas excepciones, Microsoft Rich Edit 2.0 usa las mismas funciones, estructuras y mensajes que Microsoft Rich Edit 1.0. Sin embargo, tenga en cuenta las siguientes diferencias:

-   El nombre de la clase de ventana Microsoft Rich Edit 1.0 es **RichEdit**. Microsoft Rich Edit 2.0 tiene clases de ventana ANSI y Unicode **RichEdit20A** y **RichEdit20W,** respectivamente. Para especificar la clase de ventana rich edit adecuada, use la constante RICHEDIT CLASS, que el archivo Richedit.h define en función de la definición de la \_ marca de compilación UNICODE.
-   En Microsoft Rich Edit 2.0, si crea un control de edición enriquecido Unicode (que espera mensajes de texto Unicode), solo debe especificar datos Unicode en los mensajes de ventana enviados al control. Del mismo modo, si crea un control de edición enriquecido ANSI, envíe solo datos ANSI o de juego de caracteres de doble byte (DBCS). Puede usar la función [**IsWindowUnicode para**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) determinar si un control de edición enriquecido usa mensajes de texto Unicode. Tenga en cuenta que las interfaces COM de edición enriquez usan texto Unicode a menos que encuentren un argumento de página de códigos.
-   Microsoft Rich Edit 1.0 usó combinaciones de caracteres CR/LF para los marcadores de párrafo. Microsoft Rich Edit 2.0 solo usó un carácter de retorno de carro \\ ('r'). Microsoft Rich Edit 3.0 usa solo un carácter de retorno de carro, pero puede emular Microsoft Rich Edit 1.0 en este sentido.
-   Microsoft Rich Edit 2.0 introdujo los siguientes mensajes nuevos. 

    | Message                                           | Descripción                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**EM \_ AUTOURLDETECT**](em-autourldetect.md)     | Habilita o deshabilita la detección automática de direcciones URL.                            |
    | [**EM \_ CANREDO**](em-canredo.md)                 | Determina si hay alguna acción en la cola de rehacer.             |
    | [**EM \_ GETIMECOMPMODE**](em-getimecompmode.md)   | Recupera el modo del editor de métodos de entrada (IME) actual.                   |
    | [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)   | Recupera las opciones de compatibilidad con IME y idioma asiático.                   |
    | [**EM \_ GETREDONAME**](em-getredoname.md)         | Recupera el nombre de tipo de la acción siguiente en la cola de rehacer.           |
    | [**EM \_ GETTEXTMODE**](em-gettextmode.md)         | Recupera el modo de texto o el nivel de deshacer.                                  |
    | [**EM \_ GETUNDONAME**](em-getundoname.md)         | Recupera el nombre de tipo de la acción siguiente en la cola de deshacer.           |
    | [**EM \_ REDO**](em-redo.md)                       | Rehace la acción siguiente en la cola de rehacer.                               |
    | [**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)   | Establece opciones para la compatibilidad con IME y el idioma asiático.                        |
    | [**EM \_ SETTEXTMODE**](em-settextmode.md)         | Establece el modo de texto o el nivel de deshacer.                                       |
    | [**EM \_ SETUNDOLIMIT**](em-setundolimit.md)       | Establece el número máximo de acciones de la cola de deshacer.                   |
    | [**EM \_ STOPGROUPTYPING**](em-stopgrouptyping.md) | Detiene la agrupación de acciones de escritura consecutivas en la acción de deshacer actual. |

    

     

-   Microsoft Rich Edit 2.0 introdujo las siguientes estructuras nuevas. 

    | Estructura                          | Descripción                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Contiene información sobre el formato de caracteres. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Contiene información sobre el formato de párrafo. |

    

     

-   Los mensajes siguientes solo se admiten en versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admiten en versiones posteriores de Rich Edit.

    [**EM \_ CONVPOSITION**](em-convposition.md)

    [**EM \_ GETIMECOLOR**](em-getimecolor.md)

    [**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)

    [**EM \_ GETPUNCTUATION**](em-getpunctuation.md)

    [**EM \_ GETWORDWRAPMODE**](em-getwordwrapmode.md)

    [**EM \_ SETIMECOLOR**](em-setimecolor.md)

    [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)

    [**EM \_ SETPUNCTUATION**](em-setpunctuation.md)

    [**EM \_ SETWORDWRAPMODE**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Edición enriquecte versión 3.0

Microsoft Rich Edit 3.0 es un archivo DLL único, escalable y de todo el mundo que ofrece un alto rendimiento y compatibilidad con Word en un paquete pequeño. Las nuevas características de Microsoft Rich Edit 3.0 incluyen texto más enriquecido, zoom, enlace de fuentes, compatibilidad con IME más eficaz y compatibilidad con scripts complejos enriquecidos (bidireccional, indic y tailandés).

Microsoft Rich Edit 3.0 incluye las siguientes características, además de las características proporcionadas por [Rich Edit Versión 2.0.](#rich-edit-version-20)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>El factor de zoom se da mediante una relación.</td>
</tr>
<tr class="even">
<td>Numeración de párrafos (nivel único)</td>
<td>Números numéricos, alfabéticos superiores e inferiores, o números latinos.</td>
</tr>
<tr class="odd">
<td>Tablas simples</td>
<td>La eliminación e inserción de filas es posible, pero no se puede volver a ajustar ni ajustar dentro de las celdas. Con la tipografía avanzada activada (consulte <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), Microsoft Rich Edit 3.0 puede alinear las columnas centradas o vaciar a la derecha e incluir decimales. Las celdas se simulan mediante tabulaciones, por lo que las pestañas de texto y los retornos de carro se reemplazan por espacios en blanco.</td>
</tr>
<tr class="even">
<td>Estilos normales y de encabezado</td>
<td>Los estilos de encabezado y estilo normales integrados del 1 al 9 son compatibles con las <a href="em-setparaformat.md"><strong>interfaces</strong></a> EM_SETPARAFORMAT text <a href="text-object-model.md">object model</a> (TOM).</td>
</tr>
<tr class="odd">
<td>Más tipos de subrayado</td>
<td>Se han agregado guiones, guiones, puntos de guion y subrayado de puntos.</td>
</tr>
<tr class="even">
<td>Coloración de subrayado</td>
<td>El texto subrayado se puede etiquetar con una de las 15 opciones de documento para los colores de subrayado.</td>
</tr>
<tr class="odd">
<td>Texto oculto</td>
<td>Marcado por el atributo CHARFORMAT2. Útil para el redondeo (escribir en un archivo en el que se leyó) de información que normalmente no debería mostrarse.</td>
</tr>
<tr class="even">
<td>Más teclas de acceso rápido predeterminadas</td>
<td>Estas teclas de acceso rápido funcionan igual que las de Word. Por ejemplo, teclas de acento europeo no superpuestas (solo teclados de EE. UU.). La tecla de acceso rápido de número (CTRL+L) recorrerá las opciones de numeración disponibles, empezando por una viñeta.</td>
</tr>
<tr class="odd">
<td>HexToUnicode IME</td>
<td>Permite a un usuario convertir entre hexadecimal y Unicode mediante teclas de acceso rápido.</td>
</tr>
<tr class="even">
<td>Comillas inteligentes</td>
<td>Esta característica se activa y desactiva mediante CTRL+ALT+' para teclados de EE. UU.</td>
</tr>
<tr class="odd">
<td>Guiones flexibles</td>
<td>Para texto sin formato, use 0xAD. Para RTF, use \- .</td>
</tr>
<tr class="even">
<td>Cursor cursiva</td>
<td>Además, el cursor del mouse cambia a una mano cuando se sobre las direcciones URL.</td>
</tr>
<tr class="odd">
<td>Opción de tipografía avanzada</td>
<td>Microsoft Rich Edit 3.0 puede usar una opción de tipografía avanzada para la separación de líneas y la presentación <a href="em-gettypographyoptions.md"><strong>(consulte EM_GETTYPOGRAPHYOPTIONS</strong></a>). Esta elegante opción se agregó principalmente para facilitar el control de scripts complejos (bidireccional, indic y tailandés). Además, se producen varias mejoras para scripts simples. Algunos ejemplos son:
<ul>
<li>Pestañas central, derecha y decimal</li>
<li>Texto totalmente justificado</li>
<li>Promedio de subrayado, que proporciona un subrayado uniforme incluso cuando las ejecuciones de texto adyacentes tienen tamaños de fuente diferentes.</li>
</ul></td>
</tr>
<tr class="even">
<td> Compatibilidad con escritura compleja</td>
<td>Microsoft Rich Edit 3.0 admite bidireccional (texto con árabe o hebreo mixto con otros scripts), Indic (scripts nativos como Devangari) y texto tailandés. Para admitir estos scripts complejos, se usan la tipografía avanzada y los componentes de Uniscribe.</td>
</tr>
<tr class="odd">
<td>Enlace de fuentes</td>
<td>Microsoft Rich Edit 3.0 elegirá automáticamente una fuente adecuada para los caracteres que claramente no pertenecen a la marca del juego de caracteres actual. Esto se hace asignando juegos de caracteres a ejecuciones de texto y asociando fuentes a esos juegos de caracteres. Para obtener más información, vea <a href="using-rich-edit-controls.md">Enlace de fuentes</a>.</td>
</tr>
<tr class="even">
<td>Opciones de lectura y escritura de texto sin formato específicas de los juegos de caracteres</td>
<td>Esto permite leer un archivo mediante un juego de caracteres y escribir con un juego de caracteres diferente.</td>
</tr>
<tr class="odd">
<td>UTF-8 RTF</td>
<td>Esto se recomienda para las operaciones de cortar, copiar y pegar. Este formato de archivo es más compacto que rtf normal, más rápido y compatible con Unicode.</td>
</tr>
<tr class="even">
<td>Microsoft Office compatibilidad con 9 IME (IME98)</td>
<td>Esta funcionalidad de IME más eficaz se ha separado en un módulo independiente. Características incluidas:
<ul>
<li>Reconversión En las versiones anteriores, el usuario necesitaba eliminar primero la cadena final y, a continuación, escribir una nueva cadena para llegar al candidato correcto. Esta nueva característica permite al usuario volver a convertir la cadena final al modo de composición, lo que permite una selección sencilla de una cadena candidata diferente.<br/></li>
<li>Fuente de documentos Esta característica proporciona a IME98 el texto del párrafo actual, lo que ayuda a IME98 a realizar una conversión más precisa durante la escritura.<br/></li>
<li>Operación del mouse Esta característica proporciona un mejor control sobre las ventanas candidatas y de la interfaz de usuario durante la escritura.<br/></li>
<li>Posición de la interfaz de usuario Esta característica proporciona la información de línea y el cursor de referencia actual, que IME98 usa para colocar ventanas de interfaz de usuario (por ejemplo, una lista de candidatos).<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Compatibilidad con el Administrador de métodos de entrada activo (IMM)</td>
<td>Los usuarios pueden invocar el objeto IMM activo, que permite a los usuarios escribir caracteres asiáticos en sistemas de EE. UU.</td>
</tr>
<tr class="even">
<td>Compatibilidad con HexToUnicode</td>
<td>Los usuarios pueden convertir entre la notación hexadecimal y Unicode mediante teclas de acceso rápido.</td>
</tr>
<tr class="odd">
<td>Más redondeo RTF</td>
<td>El texto RTF que se lee en un archivo se volverá a escribir intacto.</td>
</tr>
<tr class="even">
<td>Modo de compatibilidad 1.0 mejorado</td>
<td>Microsoft Rich Edit 3.0 puede emular el comportamiento de Microsoft Rich Edit 1.0. Por ejemplo, es posible cambiar entre asignaciones de mbcs y de posición de caracteres Unicode (cp).</td>
</tr>
<tr class="odd">
<td>Mayor control de inmovilización</td>
<td>La pantalla se puede inmovilizar a través de varias llamadas API y, a continuación, desconéctese para mostrar las actualizaciones.</td>
</tr>
<tr class="even">
<td>Mayor control de deshacer</td>
<td>La deshacer se puede suspender y reanudar (un requisito de IME).</td>
</tr>
<tr class="odd">
<td>Aumento o disminución del tamaño de fuente</td>
<td>Aumenta o disminuye el tamaño de fuente a uno de los seis valores estándar (12, 28, 36, 48, 72 y 80 puntos).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Edición enriquecte versión 4.1

La clase de ventana de Microsoft Rich Edit 4.1 es MSFTEDIT \_ CLASS. Las nuevas características de Microsoft Rich Edit 4.1 incluyen guiones, rotación de páginas y compatibilidad Text Services Framework (TSF).

Microsoft Rich Edit 4.1 incluye las siguientes características, además de las características proporcionadas por [Rich Edit Versión 3.0.](#rich-edit-version-30)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Etimología</td>
<td>La guión se admite a través de las siguientes API: <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc,</em></a> <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>y <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Rotación de páginas</td>
<td>El diseño de arriba a abajo y de abajo a arriba se admite mediante EM_SETPAGEROTATE <a href="em-setpagerotate.md"><strong>y</strong></a> <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Text Services Framework compatibilidad</td>
<td><ul>
<li>Para activar TSF y determinadas características de TSF, use los siguientes estilos en <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE:</strong></a>SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING y SES_CTFALLOWSMARTTAG.</li>
<li>Para establecer y obtener el sesgo del modo TSF, use <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> y <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Para establecer y obtener el estado del teclado TSF, use <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> y <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Compatibilidad adicional con IME</td>
<td><ul>
<li>Para establecer y obtener el sesgo del modo IME, use <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> y <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Para obtener las propiedades y funcionalidades del IME, use <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>.</li>
<li>Para obtener el texto de composición de IME, use <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>.</li>
<li>Para determinar si la configuración regional es una configuración regional de Asia Oriental, use <a href="em-isime.md"><strong>EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Configuración <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> adicional</td>
<td>Además de la configuración de TSF, hay nuevas opciones que excluyen los IME, establecen un flujo de texto bidireccional, usan fuentes draftmode y mucho más.</td>
</tr>
<tr class="even">
<td>Configuración <a href="em-setcharformat.md"><strong>de EM_SETCHARFORMAT</strong></a> adicional</td>
<td>Las nuevas marcas permiten al cliente establecer la fuente y los tamaños de fuente predeterminados para un LCID o juego de caracteres determinados, establecer la fuente predeterminada para el control, evitar el cambio de teclado para que coincida con la fuente, etc.</td>
</tr>
<tr class="odd">
<td>Restricción de la entrada al texto ANSI</td>
<td>El <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> en <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> impide que la entrada Unicode entre en un control Rich Edit.</td>
</tr>
<tr class="even">
<td>Notificación de palabras clave RTF no admitidas</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> a una aplicación cuando hay una palabra clave RTF no admitida.</td>
</tr>
<tr class="odd">
<td>Compatibilidad para lenguajes adicionales</td>
<td>Entre los idiomas adicionales se incluyen Armenio, Divehi, Telugu y otros.</td>
</tr>
<tr class="even">
<td>Compatibilidad mejorada con tablas</td>
<td>Entre las características se incluyen: ajuste dentro de celdas, control mejorado a través de RTF y navegación mejorada.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Se <a href="rich-edit-control-styles.md"><strong>admite ES_VERTICAL</strong></a> estilo de ventana.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a> compatibilidad</td>
<td>Para enviar o publicar caracteres Unicode en ventanas ANSI, use <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>. Es equivalente a <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, pero usa (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Funcionalidad de edición de control no admitida

Los controles de edición enriquecciones admiten la mayoría de las funciones, pero no todas, para los controles de edición multilínea. En esta sección se enumeran los mensajes de control de edición y los estilos de ventana que *no son compatibles* con los controles de edición enriquecidos.

Los siguientes mensajes se procesan mediante controles de edición, pero *no* por controles de edición enriquecidos.



| Mensaje no admitido                         | Comentarios                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**EM \_ FMTLINES**](em-fmtlines.md)         | No compatible.                                                                                                              |
| [**EM \_ GETHANDLE**](em-gethandle.md)       | Los controles de edición enriquecciones no almacenan texto como una matriz simple de caracteres.                                                       |
| [**EM \_ GETIMESTATUS**](em-getimestatus.md) | No compatible.                                                                                                              |
| [**EM \_ GETMARGINS**](em-getmargins.md)     | No compatible.                                                                                                              |
| [**EM \_ SETHANDLE**](em-sethandle.md)       | Los controles de edición enriquecciones no almacenan texto como una matriz simple de caracteres.                                                       |
| [**EM \_ SETIMESTATUS**](em-setimestatus.md) | No compatible.                                                                                                              |
| [**EM \_ SETMARGINS**](em-setmargins.md)     | Compatible con Microsoft Rich Edit 3.0.                                                                                       |
| [**EM \_ SETRECTNP**](em-setrectnp.md)       | No compatible.                                                                                                              |
| [**EM \_ SETTABSTOPS**](em-settabstops.md)   | En su lugar, se usa el mensaje [**EM \_ SETPARAFORMAT.**](em-setparaformat.md) Compatible con Microsoft Rich Edit 3.0.<br/> |
| [**WM \_ CTLCOLOR**](/windows/desktop/DevNotes/wm-ctlcolor-)    | En su lugar, se usa el mensaje [**EM \_ SETBNDCOLOR.**](em-setbkgndcolor.md)                                                  |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)        | En su lugar, se usa el mensaje [**EM \_ GETCHARFORMAT.**](em-getcharformat.md)                                                  |



 

Los siguientes estilos de ventana se usan con controles de edición multilínea, pero no con controles de edición enriquecidos: [**ES \_ LOWERCASE,**](edit-control-styles.md) [**ES \_ UPPERCASE**](edit-control-styles.md)y [**ES \_ OEMCONVERT.**](edit-control-styles.md)

## <a name="rich-edit-shortcut-keys"></a>Teclas de método abreviado rich edit

Los controles de edición enriquecciones admiten las siguientes teclas de método abreviado.



| Claves                      | Operaciones                                                                                                                               | Comentarios                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mayús+Retroceso           | Generación de un LRM/LRM en un teclado de bidi                                                                                                    | Específico de BiDi                                                                                                                                                                                                                  |
| Ctrl+Tab                  | Pestaña                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl+Borrar                | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+Panel de número 5         | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+A                    | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+T                    | Alineación del centro                                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl+J                    | Justificación de la alineación                                                                                                                        |                                                                                                                                                                                                                                |
| Ctrl+R                    | Alineación derecha                                                                                                                          |                                                                                                                                                                                                                                |
| Ctrl+L                    | Alineación izquierda                                                                                                                           |                                                                                                                                                                                                                                |
| Ctrl+C                    | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+V                    | Pegar                                                                                                                                    |                                                                                                                                                                                                                                |
| Ctrl+X                    | Cortar                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl+Z                    | Deshacer                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Y                    | Rehacer                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+'+' (Ctrl+Mayús+'=') | Superscript                                                                                                                              |                                                                                                                                                                                                                                |
| Ctrl+'='                  | Subscript                                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl+1                    | Espaciado de línea = 1 línea.                                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+2                    | Espaciado de línea = 2 líneas.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+5                    | Espaciado de línea = 1,5 líneas.                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl+' (apóstrofo)       | Acentos de acentos                                                                                                                             | Después de presionar la tecla de corte corto, presione la letra adecuada (por ejemplo, a, e o u). Esto solo se aplica a teclados en inglés, francés, alemán, italiano y español.                                                         |
| Ctrl+ \` (grave)           | Acento grave                                                                                                                             | Vea Los comentarios de Ctrl+'.                                                                                                                                                                                                           |
| Ctrl+~ (tilde)            | Tilde de acento                                                                                                                             | Vea Los comentarios de Ctrl+'.                                                                                                                                                                                                           |
| Ctrl+; (punto y coma)        | Umlaut de acento                                                                                                                            | Vea Los comentarios de Ctrl+'.                                                                                                                                                                                                           |
| Ctrl+Mayús+6              | Acento de acento (circunflejo)                                                                                                                | Vea Los comentarios de Ctrl+'.                                                                                                                                                                                                           |
| Ctrl+, (coma)            | Cedilla de acento                                                                                                                           | Vea Los comentarios de Ctrl+'.                                                                                                                                                                                                           |
| Ctrl+Mayús+' (apóstrofo) | Activación de comillas inteligentes                                                                                                                    |                                                                                                                                                                                                                                |
| Retroceso                 | Si el texto está protegido, bip y no lo elimine. De lo contrario, elimine el carácter anterior.                                                   |                                                                                                                                                                                                                                |
| Ctrl+Retroceso            | Elimine la palabra anterior. Esto genera un código \_ F16 de VK.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | Igual que retroceso.                                                                                                                       |                                                                                                                                                                                                                                |
| Ctrl+Insertar               | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Mayús+Insertar               | Pegar                                                                                                                                    |                                                                                                                                                                                                                                |
| Insertar                    | Sobrescribir                                                                                                                                | DBCS no sobrescribe.                                                                                                                                                                                                       |
| Ctrl+Flecha izquierda           | Mueva el cursor una palabra a la izquierda.                                                                                                        | En el teclado de bidi, esto depende de la dirección del texto.                                                                                                                                                                   |
| Ctrl+Flecha derecha          | Mueva el cursor una palabra a la derecha.                                                                                                       | Vea Ctrl+Comentarios de flecha izquierda.                                                                                                                                                                                                  |
| Ctrl+Mayús a la izquierda           | Alineación izquierda                                                                                                                           | En los documentos de BiDi, esto es para el orden de lectura de izquierda a derecha.                                                                                                                                                                    |
| Ctrl+Mayús a la derecha          | Alineación derecha                                                                                                                          | En los documentos de BiDi, esto es para el orden de lectura de derecha a izquierda.                                                                                                                                                                    |
| Ctrl+Flecha arriba             | Ir a la línea anterior.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Flecha abajo           | Ir a la línea siguiente.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Inicio                 | Ir al principio del documento.                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+Fin                  | Moverse al final del documento.                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl+Subir página              | Subir una página.                                                                                                                        | Si se encuentra en los controles SystemEditMode y Single Line, no haga nada.                                                                                                                                                                      |
| Ctrl+Página abajo            | Bajar una página.                                                                                                                      | Vea Ctrl+Subir comentarios.                                                                                                                                                                                                     |
| Ctrl+Supr               | Elimine la palabra siguiente o los caracteres seleccionados.                                                                                             |                                                                                                                                                                                                                                |
| Mayús+Supr              | Corte los caracteres seleccionados.                                                                                                             |                                                                                                                                                                                                                                |
| Esc                       | Detenga la función de arrastrar y colocar.                                                                                                                          | Mientras se hace una operación de arrastrar y colocar texto.                                                                                                                                                                                               |
| Alt+Esc                   | Cambie la aplicación activa.                                                                                                           |                                                                                                                                                                                                                                |
| Alt+X                     | Convierte el valor hexadecimal Unicode que precede al punto de inserción en el carácter Unicode correspondiente.                             |                                                                                                                                                                                                                                |
| Alt+Mayús+X               | Convierte el carácter Unicode que precede al punto de inserción en el valor hexadecimal Unicode correspondiente.                             |                                                                                                                                                                                                                                |
| Alt+0xxx (Panel de número)     | Inserta valores Unicode si xxx es mayor que 255. Cuando xxx es menor que 256, el texto del intervalo ASCI se inserta en función del teclado actual. | Debe especificar valores decimales.                                                                                                                                                                                                     |
| Alt+Mayús+Ctrl+F12        | Hexadecimal a Unicode.                                                                                                                          | En caso de que Alt+X ya se use para otro uso.                                                                                                                                                                                |
| Alt+Mayús+Ctrl+F11        | El texto seleccionado se mostrará en la ventana del depurador y se guardará en %temp% \\DumpFontInfo.txt.                                               | Solo para depuración (debe establecer Flag=8 en Win.ini)                                                                                                                                                                                 |
| Ctrl+Mayús+A              | Establezca todos los límites.                                                                                                                            |                                                                                                                                                                                                                                |
| Ctrl+Mayús+L              | Estilo de viñeta de Fiddle.                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Mayús+Flecha derecha    | Aumente el tamaño de fuente.                                                                                                                      | El tamaño de fuente cambia en 1 punto en el intervalo de 4pt-11pt; por 2 puntos para 12pt-28pt; cambia de 28pt -> 36pt -> 48pt -> 72pt -> 80pt; cambia en 10 puntos en el intervalo de 80pt - 1630pt; el valor máximo es 1638. |
| Ctrl+Mayús+Flecha izquierda     | Reducir el tamaño de fuente.                                                                                                                      | Vea Ctrl+Mayús+Comentarios de flecha derecha.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Controles de edición enriquecciones sin ventanas](windowless-rich-edit-controls.md)
</dt> </dl>

