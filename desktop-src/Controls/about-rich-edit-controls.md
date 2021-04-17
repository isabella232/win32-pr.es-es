---
title: Acerca de los controles Rich Edit
description: En esta sección se presentan controles Rich Edit.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95f6dc1cc1f37bf604e6c0a891f92cd20bb7af6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105656433"
---
# <a name="about-rich-edit-controls"></a>Acerca de los controles Rich Edit

Los temas siguientes se describen en esta sección.

-   [Versiones de Rich Edit](#versions-of-rich-edit)
    -   [Versión de edición enriquecida 1,0](#rich-edit-version-10)
    -   [Versión de edición enriquecida 2,0](#rich-edit-version-20)
    -   [Versión de edición enriquecida 3,0](#rich-edit-version-30)
    -   [Versión de edición enriquecida 4,1](#rich-edit-version-41)
-   [Funcionalidad de control de edición no admitida](#unsupported-edit-control-functionality)
-   [Teclas de método abreviado de edición enriquecida](#rich-edit-shortcut-keys)
-   [Temas relacionados](#related-topics)

## <a name="versions-of-rich-edit"></a>Versiones de Rich Edit

La especificación original para los controles Rich Edit es Microsoft Rich Edit 1,0; la especificación actual es Microsoft Rich Edit 4,1. Cada versión de Rich Edit es un supraconjunto de la anterior, salvo que solo las compilaciones asiáticas de Microsoft Rich Edit 1,0 tienen una opción de texto vertical. Antes de crear un control Rich Edit, debe llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para comprobar qué versión de Microsoft Rich Edit está instalada.

En la tabla siguiente se muestra qué DLL corresponde a la versión de Rich Edit. Tenga en cuenta que el nombre del archivo no cambió de la versión 2,0 a la versión 3,0. Esto permite actualizar la versión 2,0 a la versión 3,0 sin interrumpir el código existente.



| Versión de edición enriquecida | Archivo DLL          | Clase de ventana    |
|-------------------|--------------|-----------------|
| 1,0               | Riched32.dll | RICHEDIT ( \_ clase) |
| 2.0               | Riched20.dll | RICHEDIT ( \_ clase) |
| 3.0               | Riched20.dll | RICHEDIT ( \_ clase) |
| 4,1               | Msftedit.dll | \_clase MSFTEDIT |



 

### <a name="rich-edit-version-10"></a>Versión de edición enriquecida 1,0

Microsoft Rich Edit 1,0 incluye las siguientes características.



|                                                                                    |                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entrada y selección de texto                                                           | Mayor parte de la selección y la entrada de texto. Compatibilidad con la barra de selección (la barra de selección es un área no marcada a la izquierda de cada párrafo en la que se hace clic, selecciona la línea). Opciones de ajuste automático de palabra y de selección automática de palabras. Selección de uno, dos y tres clics. |
| Edición ANSI (juego de caracteres de un solo byte (SBCS) y juego de caracteres multibyte (MBCS)) | Sin embargo, no hay ninguna edición Unicode.                                                                                                                                                                                                                                                     |
| Conjunto básico de propiedades de formato de caracteres y párrafos                             | Vea [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) y [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Propiedades de formato de caracteres                                                    | Nombre y tamaño de fuente, negrita, cursiva, subrayado sólido, tachado, protegido, vínculo, desplazamiento y color del texto.                                                                                                                                                                                   |
| Propiedades de formato de párrafo                                                    | Inicio de sangría, sangría derecha, desplazamiento de línea posterior, viñeta, alineación (izquierda, centro, derecha) y tabulaciones.                                                                                                                                                                                    |
| Buscar hacia delante                                                                       | Incluye opciones que no distinguen mayúsculas de minúsculas y que coinciden con palabras completas.                                                                                                                                                                                                                                   |
| Interfaz basada en mensajes                                                            | Casi un superconjunto del conjunto de mensajes de control de edición del sistema más dos interfaces, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) y [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback).                                                                                                              |
| Objetos insertados                                                                   | Requiere la colaboración del cliente basada en las interfaces [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) y [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                          |
| Compatibilidad con menús del botón derecho                                                          | Usa la interfaz [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                                                                                                      |
| Edición de arrastrar y colocar                                                              | Se admite la edición de arrastrar y colocar.                                                                                                                                                                                                                                                       |
| Notificaciones                                                                      | [**WM \_**](/windows/desktop/menurc/wm-command) Mensajes de comandos enviados al cliente más un número de otros. Este es un superconjunto de notificaciones de control común.                                                                                                                                                 |
| Deshacer o rehacer de un solo nivel                                                             | Se comporta de forma similar al control de edición del sistema. Al seleccionar **Deshacer** , se invierte la última acción y esa acción se convierte en la nueva acción de **rehacer** .                                                                                                                                          |
| Texto vertical simple                                                               | (Solo compilaciones asiáticas).                                                                                                                                                                                                                                                                      |
| Compatibilidad con el editor de métodos de entrada (IME)                                                  | (Solo compilaciones asiáticas).                                                                                                                                                                                                                                                                      |
| Edición WYSIWYG con métricas de impresora                                              | Esta característica es necesaria para Microsoft WordPad, en particular.                                                                                                                                                                                                                              |
| Cortar/copiar/pegar/streaming/StreamOut                                                  | Con texto sin formato **( \_ texto CF**) o formato de texto enriquecido (RTF) con y sin objetos.                                                                                                                                                                                                        |
| Código base de C                                                                        | El código está escrito en C, que proporciona una base sólida y versátil.                                                                                                                                                                                                                |
| Compilaciones diferentes para distintos scripts                                             | Microsoft Rich Edit 1,0 soluciona problemas de localización con diferentes compilaciones.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Versión de edición enriquecida 2,0

Microsoft Rich Edit 2,0 incorporó varias características adicionales, como la compatibilidad con lenguajes Unicode y asiáticos, la deshacer multinivel, las interfaces del modelo de objetos componentes (COM) y numerosas mejoras en la interfaz de usuario.

Microsoft Rich Edit 2,0 incluye las siguientes características, además de las características proporcionadas por [Microsoft Rich edit 1,0](#rich-edit-version-10).



|                                               |                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode facilita el trabajo en el control de texto internacional. Sin embargo, se necesita esfuerzo para mantener la compatibilidad con los documentos que no son Unicode existentes, es decir, la capacidad de convertir a o desde texto enriquecido y sin Unicode.                                                                                                                                                             |
| Soporte internacional general                 | Algoritmo de salto de línea general (extensión de reglas Kinsoku), vinculación de fuentes simples, cambio de fuentes de teclado.                                                                                                                                                                                                                                                                          |
| Compatibilidad con idiomas asiáticos                                 | El nivel 2 (cuadro de diálogo) y 3 (alineado) se admiten en los IME.                                                                                                                                                                                                                                                                                                                            |
| Búsqueda y soporte técnico inactivo                     | Se admite la búsqueda hacia delante y hacia atrás.                                                                                                                                                                                                                                                                                                                                         |
| Compatibilidad bidireccional                         | Esto se incluye en Microsoft Rich Edit 2,1                                                                                                                                                                                                                                                                                                                                          |
| Deshacer multinivel                               | Una arquitectura de deshacer extensible permite al cliente participar en el modelo de deshacer de toda la aplicación.                                                                                                                                                                                                                                                                                         |
| Compatibilidad con el mouse Magellan                        | Este es el mouse con un rodillo para el desplazamiento.                                                                                                                                                                                                                                                                                                                                       |
| Compatibilidad con fuentes dobles                             | El teclado puede cambiar automáticamente las fuentes cuando la fuente activa no es adecuada para el teclado actual, por ejemplo, caracteres kanji en Times New Roman.                                                                                                                                                                                                                            |
| Aplicación de fuentes inteligentes                              | La solicitud de cambio de fuente no aplica fuentes occidentales a caracteres asiáticos.                                                                                                                                                                                                                                                                                                                |
| Visualización mejorada                              | Un mapa de bits no en pantalla se usa cuando se producen varias fuentes en la misma línea. Esto permite, por ejemplo, que la última letra de la palabra fría no se corte.                                                                                                                                                                                                                           |
| Compatibilidad con transparencia                          | También en modo sin ventanas.                                                                                                                                                                                                                                                                                                                                                             |
| Colores de selección del sistema                       | Se usa para seleccionar texto.                                                                                                                                                                                                                                                                                                                                                             |
| Reconocimiento de URL automático                     | Puede comprobar si hay varios formatos de dirección URL (por ejemplo, http:)                                                                                                                                                                                                                                                                                                                           |
| Compatibilidad con la interfaz de usuario de edición de Microsoft Word          | Selección, semántica del teclado del teclado.                                                                                                                                                                                                                                                                                                                                                  |
| EOP de Word Standard                             | La marca de final de párrafo (CR) también puede controlar el retorno de carro/avance de línea (CR/LF) (retorno de carro, avance de línea).                                                                                                                                                                                                                                                                       |
| Funcionalidad de texto sin formato y texto enriquecido | Formato de un solo carácter y formato de un solo párrafo.                                                                                                                                                                                                                                                                                                                                 |
| Controles de una sola línea y de varias líneas            | Truncar al principio del primer párrafo y sin WordWrap.                                                                                                                                                                                                                                                                                                                                  |
| Teclas de aceleración                              | Se admiten las teclas de aceleración.                                                                                                                                                                                                                                                                                                                                                      |
| Estilo de ventana de contraseña                         | Los controles de edición de contraseñas se proporcionan mediante [**em \_ GETPASSWORDCHAR**](em-getpasswordchar.md) y [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md).                                                                                                                                                                                                                                 |
| Arquitectura escalable                         | Para reducir el tamaño de la instancia.                                                                                                                                                                                                                                                                                                                                                             |
| Operaciones e interfaces sin ventanas           | Esto se proporciona a través de las interfaces [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) y [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .                                                                                                                                                                                                                                                                   |
| Interfaces COM duales                           | Interfaces del modelo de objetos de texto (TOM).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Se ha agregado el espesor de fuente, el color de fondo, el identificador de configuración regional, el tipo de subrayado, el superíndice y el subíndice (además del desplazamiento), efecto deshabilitado. Solo para RTF Roundtripping, se ha agregado la cantidad de espacio entre las letras, el tamaño de twip por encima del que se va a ajustar a un par de caracteres, un tipo de texto animado, varios efectos: sombra/contorno de fuente, todos los extremos, Versalitas, oculto, en relieve, en relieve y revisado. |
| PARAFORMAT2                                   | Espacio que se ha agregado antes y después y el espaciado de línea de palabras. En el caso de los Roundtripping RTF, agregue el estilo o el grosor de sombreado, la numeración de inicio/estilo/tabulador, el espacio de borde/ancho/lados, la alineación de tabulación/líderes, varios efectos de párrafo de palabra: RTL Paragraph, Keep, Keep-Next, Page-break-Before, no-line-Number, no-viuda-                                         |
| Más Roundtripping RTF                        | Todas las propiedades FormatFont y FormatParagraph de Word.                                                                                                                                                                                                                                                                                                                           |
| Estabilidad y estabilización del código              | Ejemplos: validación de parámetros y objetos, invariantes de función, protecciones de reentrada y estabilización de objetos.                                                                                                                                                                                                                                                                             |
| Infraestructura de pruebas sólidas                 | Incluye pruebas de regresión extensas.                                                                                                                                                                                                                                                                                                                                               |
| rendimiento mejorado.                          | Espacio de trabajo más pequeño, tiempos de carga y representación más rápidos, etc.                                                                                                                                                                                                                                                                                                                     |
| Código base de C++                                 | El código está escrito en C++, que proporciona una base sólida sobre la que se va a compilar la edición enriquecida de Microsoft 3,0.                                                                                                                                                                                                                                                                             |



 

Con algunas excepciones, Microsoft Rich Edit 2,0 usa las mismas funciones, estructuras y mensajes que Microsoft Rich Edit 1,0. Sin embargo, tenga en cuenta las siguientes diferencias:

-   El nombre de la clase de ventana de Microsoft Rich Edit 1,0 es **RichEdit**. Microsoft Rich Edit 2,0 tiene las clases de ventana ANSI y Unicode **RichEdit20A** y **RichEdit20W,** respectivamente. Para especificar la clase de ventana de edición enriquecida adecuada, use la \_ constante de clase RichEdit, que define el archivo RichEdit. h, dependiendo de la definición de la marca de compilación Unicode.
-   En Microsoft Rich Edit 2,0, si crea un control Rich Edit de Unicode (uno que espera mensajes de texto Unicode), solo debe especificar datos Unicode en cualquier mensaje de ventana que se envíe al control. Del mismo modo, si crea un control Rich Edit de ANSI, solo envía datos del juego de caracteres ANSI o de doble byte (DBCS). Puede usar la función [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar si un control Rich Edit usa mensajes de texto Unicode. Tenga en cuenta que las interfaces COM de Rich Edit usan texto Unicode a menos que encuentren un argumento de página de códigos.
-   Microsoft Rich Edit 1,0 usó combinaciones de caracteres CR/LF para marcadores de párrafo. Microsoft Rich Edit 2,0 solo usó un carácter de retorno de carro (' \\ r '). Microsoft Rich Edit 3,0 solo usa un carácter de retorno de carro, pero puede emular Microsoft Rich Edit 1,0 en este sentido.
-   Microsoft Rich Edit 2,0 presentó los siguientes mensajes nuevos. 

    | Message                                           | Descripción                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**\_AUTOURLDETECT em**](em-autourldetect.md)     | Habilita o deshabilita la detección automática de direcciones URL.                            |
    | [**de \_ em**](em-canredo.md)                 | Determina si hay alguna acción en la cola de puesta al día.             |
    | [**\_GETIMECOMPMODE em**](em-getimecompmode.md)   | Recupera el modo del editor de métodos de entrada (IME) actual.                   |
    | [**\_GETLANGOPTIONS em**](em-getlangoptions.md)   | Recupera opciones para la compatibilidad con los idiomas IME y asiático.                   |
    | [**\_GETREDONAME em**](em-getredoname.md)         | Recupera el nombre de tipo de la siguiente acción en la cola de puesta al día.           |
    | [**\_GETTEXTMODE em**](em-gettextmode.md)         | Recupera el nivel de modo de texto o de deshacer.                                  |
    | [**\_GETUNDONAME em**](em-getundoname.md)         | Recupera el nombre de tipo de la acción siguiente en la cola de deshacer.           |
    | [**rehacer EM \_**](em-redo.md)                       | Rehace la siguiente acción en la cola de puesta al día.                               |
    | [**\_SETLANGOPTIONS em**](em-setlangoptions.md)   | Establece opciones para la compatibilidad con los idiomas IME y asiático.                        |
    | [**\_SETTEXTMODE em**](em-settextmode.md)         | Establece el modo de texto o el nivel de deshacer.                                       |
    | [**\_SETUNDOLIMIT em**](em-setundolimit.md)       | Establece el número máximo de acciones en la cola de deshacer.                   |
    | [**\_STOPGROUPTYPING em**](em-stopgrouptyping.md) | Detiene la agrupación de acciones de tipos consecutivas en la acción de deshacer actual. |

    

     

-   Microsoft Rich Edit 2,0 presentó las siguientes nuevas estructuras. 

    | Estructura                          | Descripción                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Contiene información sobre el formato de caracteres. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Contiene información sobre el formato de los párrafos. |

    

     

-   Los mensajes siguientes solo se admiten en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admiten en las versiones posteriores de Rich Edit.

    [**\_CONVPOSITION em**](em-convposition.md)

    [**\_GETIMECOLOR em**](em-getimecolor.md)

    [**\_GETIMEOPTIONS em**](em-getimeoptions.md)

    [**\_GETPUNCTUATION em**](em-getpunctuation.md)

    [**\_GETWORDWRAPMODE em**](em-getwordwrapmode.md)

    [**\_SETIMECOLOR em**](em-setimecolor.md)

    [**\_SETIMEOPTIONS em**](em-setimeoptions.md)

    [**\_SETPUNCTUATION em**](em-setpunctuation.md)

    [**\_SETWORDWRAPMODE em**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Versión de edición enriquecida 3,0

Microsoft Rich Edit 3,0 es un archivo DLL de un solo ancho y escalable que ofrece alto rendimiento y compatibilidad con Word en un paquete pequeño. Las nuevas características de Microsoft Rich Edit 3,0 incluyen texto más completo, zoom, enlace de fuentes, compatibilidad con IME más eficaz y completa compatibilidad con scripts complejos (bidireccional, India y tailandés).

Microsoft Rich Edit 3,0 incluye las siguientes características, además de las características proporcionadas por la [versión de edición enriquecida 2,0](#rich-edit-version-20).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>El factor de zoom se proporciona mediante una relación.</td>
</tr>
<tr class="even">
<td>Numeración de párrafos (de un solo nivel)</td>
<td>Numérico, alfabético superior o inferior, o número romano.</td>
</tr>
<tr class="odd">
<td>Tablas simples</td>
<td>La eliminación e inserción de filas es posible, pero no se cambia el tamaño ni se ajusta dentro de las celdas. Con la Tipografía avanzada activada (vea <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), Microsoft Rich Edit 3,0 puede alinear columnas centradas o vacías, e incluir decimales. Las celdas se simulan por pestañas, por lo que las pestañas de texto y los retornos de carro se reemplazan por espacios en blanco.</td>
</tr>
<tr class="even">
<td>Estilos normales y de encabezado</td>
<td>Los estilos de encabezado y estilo normal integrados se admiten en las interfaces de <a href="em-setparaformat.md"><strong>EM_SETPARAFORMAT</strong></a> y del <a href="text-object-model.md">modelo de objetos de texto</a> (Tom).</td>
</tr>
<tr class="odd">
<td>Más tipos de subrayado</td>
<td>Se ha agregado el subrayado de guiones, guiones, puntos y guiones, puntos y puntos.</td>
</tr>
<tr class="even">
<td>Colorear subrayado</td>
<td>El texto subrayado se puede etiquetar con una de las 15 opciones de documento para los colores de subrayado.</td>
</tr>
<tr class="odd">
<td>Texto oculto</td>
<td>Marcado por el atributo CHARFORMAT2. Útil para Roundtripping (escribir en un archivo en el que se leyó) la información que normalmente no debería mostrarse.</td>
</tr>
<tr class="even">
<td>Teclas de acceso rápido más predeterminadas</td>
<td>Estas teclas de acceso rápido funcionan igual que las de Word. Por ejemplo, las claves de inactividad de acentos europeos (solo teclados de EE. UU.). La tecla de acceso rápido de número (CTRL + L) recorre en iteración las opciones de numeración disponibles, empezando por la viñeta.</td>
</tr>
<tr class="odd">
<td>HexToUnicode IME</td>
<td>Permite a un usuario convertir entre hexadecimales y Unicode mediante el uso de teclas de acceso rápido.</td>
</tr>
<tr class="even">
<td>Comillas inteligentes</td>
<td>Para activar y desactivar esta característica, presione CTRL + ALT + ' para teclados de EE. UU..</td>
</tr>
<tr class="odd">
<td>Guiones flexibles</td>
<td>Para texto sin formato, use 0xAD. En el caso de RTF, use \- .</td>
</tr>
<tr class="even">
<td>Cursor en cursiva</td>
<td>Además, el cursor del mouse cambia a una mano cuando se superan las direcciones URL.</td>
</tr>
<tr class="odd">
<td>Advanced Typography, opción</td>
<td>Microsoft Rich Edit 3,0 puede usar una opción de Tipografía avanzada para la visualización y el salto de línea (consulte <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Esta opción elegante se agregó principalmente para facilitar la administración de scripts complejos (bidireccionales, Indias y tailandés). Además, se producen varias mejoras para scripts simples. Algunos ejemplos son:
<ul>
<li>Pestañas centro, derecha, decimal</li>
<li>Texto totalmente justificado</li>
<li>Aplicar el promedio de subrayado, que proporciona un subrayado uniforme incluso cuando las ejecuciones de texto adyacentes tienen tamaños de fuente diferentes.</li>
</ul></td>
</tr>
<tr class="even">
<td> Compatibilidad con escritura compleja</td>
<td>Microsoft Rich Edit 3,0 admite bidireccionales (texto con árabe o hebreo mezclado con otros scripts), lenguas indias (como Devangari) y texto tailandés. Para la compatibilidad con estos scripts complejos, se usan los componentes de Tipografía avanzada y de Uniscribe.</td>
</tr>
<tr class="odd">
<td>Enlace de fuentes</td>
<td>Microsoft Rich Edit 3,0 elegirá automáticamente una fuente adecuada para los caracteres que no pertenezcan claramente al sello del juego de caracteres actual. Para ello, se asignan juegos de caracteres a las ejecuciones de texto y se asocian las fuentes a dichos conjuntos de caracteres. Para obtener más información, vea <a href="using-rich-edit-controls.md">enlace de fuentes</a>.</td>
</tr>
<tr class="even">
<td>Opciones de lectura y escritura de texto sin formato específicas de los juegos de caracteres</td>
<td>Esto permite leer un archivo con un juego de caracteres y escribir con un juego de caracteres diferente.</td>
</tr>
<tr class="odd">
<td>RTF UTF-8</td>
<td>Esto se recomienda para cortar, copiar y pegar operaciones. Este formato de archivo es más compacto que el RTF normal, más rápido y compatible con Unicode.</td>
</tr>
<tr class="even">
<td>Compatibilidad con IME de Microsoft Office 9 (IME98)</td>
<td>Esta capacidad de IME más eficaz se ha separado en un módulo independiente. Características incluidas:
<ul>
<li>Reconversión en las versiones anteriores, el usuario necesitaba eliminar primero la cadena final y, a continuación, escribir una nueva cadena para llegar al candidato correcto. Esta nueva característica permite al usuario volver a convertir la cadena final en el modo de composición, lo que permite una fácil selección de una cadena candidata diferente.<br/></li>
<li>Fuente de documentos esta característica proporciona IME98 con el texto del párrafo actual, lo que ayuda a IME98 a realizar una conversión más precisa durante la escritura.<br/></li>
<li>Operación del mouse esta característica proporciona un mejor control sobre las ventanas candidato e interfaz de usuario durante la escritura.<br/></li>
<li>Posición del símbolo de intercalación esta característica proporciona la información de línea y el símbolo de intercalación actual, que IME98 usa para colocar ventanas de interfaz de usuario (por ejemplo, una lista de candidatos).<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Compatibilidad con el administrador de métodos de entrada (IMM) activo</td>
<td>Los usuarios pueden invocar el objeto IMM activo, que permite a los usuarios escribir caracteres asiáticos en sistemas estadounidenses.</td>
</tr>
<tr class="even">
<td>Compatibilidad con HexToUnicode</td>
<td>Los usuarios pueden realizar conversiones entre notación hexadecimal y Unicode mediante el uso de teclas de acceso rápido.</td>
</tr>
<tr class="odd">
<td>Más Roundtripping RTF</td>
<td>El texto RTF que se lee en un archivo se escribirá intacto.</td>
</tr>
<tr class="even">
<td>Modo de compatibilidad 1,0 mejorado</td>
<td>Microsoft Rich Edit 3,0 puede emular el comportamiento de Microsoft Rich Edit 1,0. Por ejemplo, es posible cambiar entre las asignaciones de la posición de caracteres Unicode (CP) y MBCS.</td>
</tr>
<tr class="odd">
<td>Aumento del control Freeze</td>
<td>La presentación se puede inmovilizar en varias llamadas API y, a continuación, descongelar para mostrar las actualizaciones.</td>
</tr>
<tr class="even">
<td>Mayor control de deshacer</td>
<td>Deshacer se puede suspender y reanudar (un requisito de IME).</td>
</tr>
<tr class="odd">
<td>Aumentar o reducir el tamaño de fuente</td>
<td>Aumenta o disminuye el tamaño de fuente a uno de los seis valores estándar (12, 28, 36, 48, 72 y 80 puntos).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Versión de edición enriquecida 4,1

La clase de ventana para Microsoft Rich Edit 4,1 es la \_ clase MSFTEDIT. Las nuevas características de Microsoft Rich Edit 4,1 incluyen guiones, rotación de páginas y compatibilidad con la plataforma de servicios de texto (TSF).

Microsoft Rich Edit 4,1 incluye las siguientes características, además de las características proporcionadas por la [versión de edición enriquecida 3,0](#rich-edit-version-30).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>División</td>
<td>La división en guiones se admite a través de las siguientes API: <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>, <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>y <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Rotación de páginas</td>
<td>El diseño de arriba abajo y de abajo a arriba se admite a través de <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> y <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Compatibilidad con el marco de trabajo de servicios de texto</td>
<td><ul>
<li>Para activar TSF y ciertas características de TSF, use los siguientes estilos en <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>: SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING y SES_CTFALLOWSMARTTAG.</li>
<li>Para establecer y obtener la diferencia del modo TSF, use <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> y <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Para establecer y obtener el estado del teclado de TSF, use <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> y <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Compatibilidad con IME adicional</td>
<td><ul>
<li>Para establecer y obtener la diferencia del modo IME, use <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> y <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Para obtener las propiedades y capacidades del IME, use <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>.</li>
<li>Para obtener el texto de composición del IME, use <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>.</li>
<li>Para determinar si la configuración regional es una configuración regional asiática oriental, use <a href="em-isime.md"><strong>EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Configuración de <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> adicional</td>
<td>Además de la configuración de TSF, hay nuevas opciones que excluyen los IME, establecen el flujo de texto bidireccional, usan fuentes draftmode, etc.</td>
</tr>
<tr class="even">
<td>Configuración de <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> adicional</td>
<td>Las nuevas marcas permiten al cliente establecer los tamaños de fuente y fuente predeterminados para un LCID o juego de caracteres determinado, para establecer la fuente predeterminada del control, para evitar que el cambio de teclado coincida con la fuente, etc.</td>
</tr>
<tr class="odd">
<td>Restringir la entrada a texto ANSI</td>
<td>El uso de <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> en <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> impide que la entrada Unicode escriba un control Rich Edit.</td>
</tr>
<tr class="even">
<td>Notificación de palabra clave RTF no admitida</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> advierte a una aplicación cuando hay una palabra clave RTF no admitida.</td>
</tr>
<tr class="odd">
<td>Compatibilidad para lenguajes adicionales</td>
<td>Otros idiomas son armenio, Divehi, Telugu y otros.</td>
</tr>
<tr class="even">
<td>Compatibilidad con tablas mejorada</td>
<td>Entre las características se incluyen: ajustar dentro de las celdas, mejorar el control a través de RTF y mejorar la navegación.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Se admite el estilo de ventana <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</td>
</tr>
<tr class="even">
<td>Compatibilidad con <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a></td>
<td>Para enviar o exponer caracteres Unicode en ventanas ANSI, use <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>. Es equivalente a <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, pero usa (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Funcionalidad de control de edición no admitida

Los controles Rich Edit admiten la mayoría de las funcionalidades, pero no todas, para los controles de edición multilínea. En esta sección se enumeran los mensajes de control de edición y los estilos de ventana que *no* son compatibles con los controles Rich Edit.

Los siguientes mensajes los procesan los controles de edición, pero *no* los controles Rich Edit.



| Mensaje no admitido                         | Comentarios                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_FMTLINES em**](em-fmtlines.md)         | No se admite.                                                                                                              |
| [**GETHANDLE (EM) \_**](em-gethandle.md)       | Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.                                                       |
| [**\_GETIMESTATUS em**](em-getimestatus.md) | No se admite.                                                                                                              |
| [**\_GETMARGINS em**](em-getmargins.md)     | No se admite.                                                                                                              |
| [**\_SETHANDLE em**](em-sethandle.md)       | Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.                                                       |
| [**\_SETIMESTATUS em**](em-setimestatus.md) | No se admite.                                                                                                              |
| [**\_SETMARGINS em**](em-setmargins.md)     | Compatible con Microsoft Rich Edit 3,0.                                                                                       |
| [**\_SETRECTNP em**](em-setrectnp.md)       | No se admite.                                                                                                              |
| [**\_SETTABSTOPS em**](em-settabstops.md)   | En su lugar, se utiliza el mensaje [**\_ SETPARAFORMAT em**](em-setparaformat.md) . Compatible con Microsoft Rich Edit 3,0.<br/> |
| [**CTLCOLOR de WM \_**](/windows/desktop/DevNotes/wm-ctlcolor-)    | En su lugar, se utiliza el mensaje [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .                                                  |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)        | En su lugar, se utiliza el mensaje [**\_ GETCHARFORMAT em**](em-getcharformat.md) .                                                  |



 

Los siguientes estilos de ventana se usan con controles de edición multilínea, pero no con controles Rich Edit: [**es \_ minúsculas**](edit-control-styles.md), [**es en \_ mayúsculas**](edit-control-styles.md)y [**es \_ OEMCONVERT**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Teclas de método abreviado de edición enriquecida

Los controles Rich Edit admiten las siguientes teclas de método abreviado.



| Claves                      | Operaciones                                                                                                                               | Comentarios                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mayús + retroceso           | Generación de un LRM/LRM en un teclado bidireccional                                                                                                    | Específico de BiDi                                                                                                                                                                                                                  |
| Ctrl+Tab                  | Pestaña                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl + borrar                | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl + almohadilla número 5         | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+A                    | Seleccionar todo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+T                    | Alineación central                                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl+J                    | Alineación de justificación                                                                                                                        |                                                                                                                                                                                                                                |
| Ctrl+R                    | Alineación a la derecha                                                                                                                          |                                                                                                                                                                                                                                |
| Ctrl+L                    | Alineación izquierda                                                                                                                           |                                                                                                                                                                                                                                |
| Ctrl+C                    | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+V                    | Pegar                                                                                                                                    |                                                                                                                                                                                                                                |
| Ctrl+X                    | Cortar                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl+Z                    | Deshacer                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Y                    | Rehacer                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl + ' + ' (Ctrl + Mayús + ' = ') | Superscript                                                                                                                              |                                                                                                                                                                                                                                |
| Ctrl + ' = '                  | Subscript                                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl+1                    | Interlineado = 1 línea.                                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+2                    | Interlineado = 2 líneas.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+5                    | Interlineado = 1,5 líneas.                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl + ' (apóstrofo)       | Acento agudo                                                                                                                             | Después de presionar la tecla de corte corto, presione la letra adecuada (por ejemplo, a, e o u). Esto se aplica solo a los teclados inglés, Francés, alemán, Italiano y español.                                                         |
| Ctrl + \` (acento grave)           | Acento grave                                                                                                                             | Vea los comentarios de Ctrl + '.                                                                                                                                                                                                           |
| Ctrl + ~ (tilde)            | Tilde de acento                                                                                                                             | Vea los comentarios de Ctrl + '.                                                                                                                                                                                                           |
| Ctrl +; punto y coma        | Diéresis de acentos                                                                                                                            | Vea los comentarios de Ctrl + '.                                                                                                                                                                                                           |
| Ctrl + Mayús + 6              | Acento circunflejo (acento circunflejo)                                                                                                                | Vea los comentarios de Ctrl + '.                                                                                                                                                                                                           |
| Ctrl +, (coma)            | Acento cedilla                                                                                                                           | Vea los comentarios de Ctrl + '.                                                                                                                                                                                                           |
| Ctrl + Mayús + ' (apóstrofo) | Activar comillas inteligentes                                                                                                                    |                                                                                                                                                                                                                                |
| Retroceso                 | Si el texto está protegido, beep y no lo elimina. De lo contrario, elimine el carácter anterior.                                                   |                                                                                                                                                                                                                                |
| Ctrl+Retroceso            | Eliminar palabra anterior. Esto genera un \_ Código tecla F16 de VK.                                                                                     |                                                                                                                                                                                                                                |
| Tecla F16                       | Igual que el retroceso.                                                                                                                       |                                                                                                                                                                                                                                |
| Ctrl+Insertar               | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Mayús+Insertar               | Pegar                                                                                                                                    |                                                                                                                                                                                                                                |
| Insertar                    | Sobrescribir                                                                                                                                | DBCS no sobrescribe.                                                                                                                                                                                                       |
| Ctrl+Flecha izquierda           | Mueve el cursor una palabra hacia la izquierda.                                                                                                        | En el teclado Bidi, esto depende de la dirección del texto.                                                                                                                                                                   |
| Ctrl+Flecha derecha          | Mueve el cursor una palabra hacia la derecha.                                                                                                       | Vea Ctrl + comentario de flecha izquierda.                                                                                                                                                                                                  |
| Ctrl + Mayús Izq           | Alineación izquierda                                                                                                                           | En documentos bidireccionales, es para el orden de lectura de izquierda a derecha.                                                                                                                                                                    |
| Ctrl + Mayús derecha          | Alineación a la derecha                                                                                                                          | En documentos bidireccionales, es para el orden de lectura de derecha a izquierda.                                                                                                                                                                    |
| Ctrl+Flecha arriba             | Desplácese a la línea anterior.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Flecha abajo           | Desplácese a la línea siguiente.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Inicio                 | Moverse al principio del documento.                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+Fin                  | Moverse al final del documento.                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl + re pág              | Subir una página.                                                                                                                        | Si está en SystemEditMode y el control de una sola línea, no haga nada.                                                                                                                                                                      |
| Ctrl + Av Pág            | Bajar una página.                                                                                                                      | Vea Ctrl + Re Pág (comentarios).                                                                                                                                                                                                     |
| Ctrl+Supr               | Eliminar la palabra siguiente o los caracteres seleccionados.                                                                                             |                                                                                                                                                                                                                                |
| Mayús+Supr              | Cortar los caracteres seleccionados.                                                                                                             |                                                                                                                                                                                                                                |
| Esc                       | Detener arrastrar y colocar.                                                                                                                          | Mientras se realiza una operación de arrastrar y colocar texto.                                                                                                                                                                                               |
| ALT + ESC                   | Cambiar la aplicación activa.                                                                                                           |                                                                                                                                                                                                                                |
| Alt+X                     | Convierte el valor hexadecimal Unicode que precede al punto de inserción en el carácter Unicode correspondiente.                             |                                                                                                                                                                                                                                |
| Alt + Mayús + X               | Convierte el carácter Unicode que precede al punto de inserción en el valor hexadecimal Unicode correspondiente.                             |                                                                                                                                                                                                                                |
| Alt + 0XXX (panel numérico)     | Inserta valores Unicode si XXX es mayor que 255. Cuando xxx es menor que 256, el texto de intervalo de ASCI se inserta en función del teclado actual. | Debe escribir valores decimales.                                                                                                                                                                                                     |
| Alt + Mayús + Ctrl + F12        | Hexadecimal a Unicode.                                                                                                                          | En caso de que ya se haya utilizado ALT + X para otro uso.                                                                                                                                                                                |
| Alt + Mayús + Ctrl + F11        | El texto seleccionado se mostrará en la ventana del depurador y se guardará en% Temp% \\DumpFontInfo.txt.                                               | Solo para depurar (debe establecer Flag = 8 en Win.ini)                                                                                                                                                                                 |
| Ctrl+Mayús+A              | Establecer todos los extremos.                                                                                                                            |                                                                                                                                                                                                                                |
| Ctrl+Mayús+L              | Estilo de viñeta de Fiddler.                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Mayús+Flecha derecha    | Aumentar el tamaño de fuente.                                                                                                                      | El tamaño de fuente cambia en 1 punto en el intervalo 4PT-11pt; por 2points para 12 PTO-28pt; cambia de 28pt-> 36pt-> 48pt-> 72pt-> 80pt; cambia en 10 puntos en el intervalo 80pt-1630pt; el valor máximo es 1638. |
| Ctrl+Mayús+Flecha izquierda     | Reducir el tamaño de fuente.                                                                                                                      | Vea Ctrl + Mayús + Flecha derecha.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Controles Rich Edit sin ventanas](windowless-rich-edit-controls.md)
</dt> </dl>

