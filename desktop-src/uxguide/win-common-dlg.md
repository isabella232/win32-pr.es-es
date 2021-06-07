---
title: Cuadros de diálogo comunes
description: Los cuadros de diálogo comunes de Microsoft Windows constan de los cuadros de diálogo Abrir archivo, Guardar archivo, Abrir carpeta, Buscar y reemplazar, Imprimir, Configuración de página, Fuente y Color.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9d64dee640037fe70b88c10294ed04bfbc74fac4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443686"
---
# <a name="common-dialogs"></a>Cuadros de diálogo comunes

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Los cuadros de diálogo comunes de Microsoft Windows constan de los cuadros de diálogo Abrir archivo, Guardar archivo, Abrir carpeta, Buscar y reemplazar, Imprimir, Configuración de página, Fuente y Color.

## <a name="open-file"></a>Abrir archivo

![captura de pantalla del cuadro de diálogo abrir ](images/win-common-dlg-image1.png)

Abrir archivo está optimizado para buscar rápidamente elementos que se usarán con un programa.

## <a name="save-file"></a>Guardar archivo

![captura de pantalla del cuadro de diálogo Guardar como ](images/win-common-dlg-image2.png)

Guardar archivo cierra el bucle guardando un archivo con sus metadatos.

## <a name="open-folder"></a>Abrir carpeta

![captura de pantalla del cuadro de diálogo Buscar archivos o carpetas ](images/win-common-dlg-image3.png)

Abrir carpeta es específicamente para elegir carpetas.

## <a name="find-and-replace"></a>Buscar y reemplazar

![captura de pantalla de los cuadros de diálogo buscar y reemplazar ](images/win-common-dlg-image4.png)

Buscar permite a los usuarios buscar cadenas de texto, mientras que reemplazar versión permite opcionalmente a los usuarios reemplazar coincidencias por otra cadena.

## <a name="print"></a>Impresión

![captura de pantalla del cuadro de diálogo de impresión ](images/win-common-dlg-image5.png)

La impresión permite a los usuarios seleccionar qué imprimir, el número de copias que se imprimen y la secuencia de intercalación, junto con la capacidad de elegir y configurar impresoras.

## <a name="page-setup"></a>Configurar página

![captura de pantalla del cuadro de diálogo de configuración de página ](images/win-common-dlg-image6.png)

La configuración de la página permite a los usuarios seleccionar el tamaño y el origen del papel, la orientación de la página y los márgenes.

## <a name="font"></a>Fuente

![captura de pantalla del cuadro de diálogo de fuente ](images/win-common-dlg-image7.png)

Fuente muestra las fuentes y los tamaños de punto de las fuentes instaladas disponibles.

## <a name="color"></a>Color

![captura de pantalla del cuadro de diálogo Editar colores ](images/win-common-dlg-image8.png)

El color permite a los usuarios seleccionar un color, ya sea a través de un conjunto predefinido de colores o eligiendo un color "personalizado".

## <a name="design-concepts"></a>Conceptos de diseño

Al usar los diálogos comunes, puede proporcionar a los usuarios una experiencia coherente en distintos programas. Y mediante el uso de los diálogos comunes, también ayuda a ofrecer a los usuarios una experiencia eficaz y divertida.

Puede mejorar significativamente la experiencia de los usuarios con estos diálogos eligiendo los valores predeterminados más adecuados para:

-   Valores de entrada (ejemplos: carpetas predeterminadas, nombres de archivo predeterminados).
-   Opciones seleccionadas (ejemplos: impresora seleccionada, opciones de impresión).
-   Vistas (ejemplos: mostrar imágenes en vista en miniatura, mostrar imágenes sin nombres de archivo, ordenar por fecha, anchos de columna).
-   Presentación (ejemplos: tamaño de la ventana, ubicación y contenido).

Debe determinar los valores predeterminados iniciales y los valores predeterminados posteriores. Los valores predeterminados iniciales los determina el programa y se basan en el uso esperado del usuario de destino, mientras que los valores predeterminados posteriores se basan en el uso real. El uso pasado es el mejor indicador del uso futuro.

¿Son eficaces los valores predeterminados del programa? Supervise el número de pasos que deben seguir los usuarios para realizar las tareas más comunes. Si los usuarios tienen que repetir los mismos pasos, posiblemente innecesarios cada vez que realizan una tarea, se pueden mejorar los valores predeterminados.

**Si solo hace una cosa...**

Proporcionar a los usuarios una experiencia eficaz y divertida mediante la selección de los valores predeterminados iniciales y posteriores adecuados.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

**¡Sí! Use los cuadros de diálogo comunes para una experiencia de usuario coherente. No cree los suyos propios.** Es especialmente difícil crear uri personalizadas que naveguen por el espacio de nombres de forma correcta y segura. Tenga en cuenta que puede personalizar los diálogos comunes si es necesario.

Para Windows Vista, Abrir archivo y Guardar archivo tienen una nueva arquitectura extensible para facilitar la exposición de funcionalidades adicionales. Este mecanismo es lo suficientemente flexible como para cumplir los requisitos mínimos de los principales proveedores de software independientes (ISV), pero no se ve roto por futuras versiones de Windows.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   Cuando corresponda, proporcione [alternativas más directas o modelesas.](glossary.md) Permitir a los usuarios:
    -   Abra los archivos al quitarlos en el programa.
    -   Guarde los archivos con su nombre y ubicación actuales con un comando Guardar.
    -   Busque la siguiente aparición de una cadena mediante la tecla F3.
    -   Imprima una copia de un documento completo en la impresora predeterminada con un comando Imprimir.
    -   Cambie las fuentes y los atributos de fuente mediante una barra de herramientas o una ventana de paleta.
    -   Cambie los colores mediante una barra de herramientas o una ventana de paleta.
-   Use los comandos siguientes para mostrar cuadros de diálogo comunes (dados junto con sus claves de [acceso preferidas):](glossary.md)



| Cuadro de diálogo común          | Comando                                 |
|------------------------|-----------------------------------------|
| Abrir archivo<br/>         | Abrir...<br/>                            |
| Guardar archivo<br/>         | Guardar como...<br/>                         |
| Abrir carpeta<br/>       | Abrir carpeta... o Elegir carpeta...<br/> |
| Buscar y reemplazar<br/>  | Encontrar... o Reemplazar...<br/>              |
| Impresión<br/>             | Imprimir...<br/>                           |
| Configurar página<br/>        | Configuración de página...<br/>                      |
| Fuente<br/>              | Fuente... o elija la fuente...<br/>          |
| Color<br/>             | Color... o Elegir color...<br/>        |



 

-   Puede usar comandos más específicos, según corresponda. Ejemplo: para exportar un archivo, use el comando Exportar archivo en lugar de Guardar como.
-   Establezca el título del cuadro de diálogo para reflejar el comando que lo inició. Ejemplo: si se inicia Guardar archivo desde un comando Exportar archivo, cambie el nombre del cuadro de diálogo a Exportar archivo.

### <a name="open-file"></a>Abrir archivo

-   Para la carpeta predeterminada inicial, use una carpeta especializada (Imágenes, Música, Vídeos) según corresponda; de lo contrario, use Documentos.
-   Para las carpetas predeterminadas posteriores, use la última carpeta abierta por el usuario mediante el programa.
-   Al abrir archivos de fotos, suprime los nombres de archivo de forma predeterminada. Las fotos normalmente se identifican por sus miniaturas y sus nombres normalmente no son significativos.

### <a name="save-file"></a>Guardar archivo

-   Para la carpeta predeterminada inicial (si se guarda un archivo nuevo por primera vez), use la carpeta especializada (Imágenes, Música, Vídeos) según corresponda; en caso contrario, use Documentos.
-   Para los archivos temporales, use la carpeta temporal del usuario actual. Elija nombres de archivo sin formato, pero únicos. Ejemplo: use File0001.tmp en lugar de ~DF1A92.tmp.
    -   **Desarrolladores:** Puede obtener la carpeta temporal del usuario actual mediante la función de API GetTempPath.
-   Para el nombre de archivo predeterminado inicial, use un nombre predeterminado único basado en:
    -   El contenido del archivo, si se conoce. Ejemplo: las primeras palabras de un documento.
    -   Patrón elegido por el usuario. Ejemplo: si el archivo anterior se denominaba "Hawái 1.jpg", elija "Hawái 2.jpg" como archivo siguiente.
    -   Patrón genérico basado en el tipo de archivo. Ejemplo: "Photo1.jpg".
-   Para los valores predeterminados posteriores (si el archivo ya existe), use la carpeta y el nombre actuales del archivo.
-   Al guardar un archivo, conserve su fecha de creación. Si el programa guarda archivos mediante la creación de un archivo temporal, elimina el original y cambia el nombre del archivo temporal al nombre de archivo original, asegúrese de copiar la fecha de creación del archivo original.
-   Use Guardar archivo si el usuario selecciona el comando Guardar sin especificar un nombre de archivo.

### <a name="file-types-lists"></a>Listas de tipos de archivo

**Nota:** Open File y Save File usan listas de tipos de archivo para determinar los tipos de archivos que se muestran y la extensión de archivo predeterminada.

-   Si la lista de tipos de archivo es corta (cinco o menos), ordene la lista por probabilidad de uso. Si la lista es larga (seis o más), use un orden alfabético para facilitar la búsqueda de los tipos.
-   En Guardar archivo, incluya todas las variaciones de las extensiones de archivo admitidas, aunque no sea habitual, y coloque primero la extensión más común. La lógica de control de archivos examina esta lista para determinar si el usuario proporcionó una extensión de archivo compatible. Ejemplo: si una lista de tipos de archivo JPEG solo incluye .jpg y .jpeg, el archivo test.jpe podría guardarse como test.jpe.jpg.
-   En Guardar archivo, el tipo de archivo predeterminado inicial es el más probable elegido por el usuario de destino. El valor predeterminado posterior es el tipo actual del archivo.
-   En Abrir archivo, el tipo de archivo predeterminado inicial es el más probable elegido por el usuario de destino. El valor predeterminado posterior debe ser el último tipo de archivo utilizado.
-   Para Abrir archivo, incluya una entrada "Todos los archivos" como primer elemento si los usuarios pueden abrir cualquier tipo de archivo o es posible que deba ver todos los archivos de una carpeta al mismo tiempo. Considere la posibilidad de proporcionar otros metadatos, como "Todas las imágenes", "Toda la música" y "Todos los vídeos". Coloque estos archivos inmediatamente después de "Todos los archivos".
-   Use el formato "Nombre de tipo de archivo ( \* .ext1; \* . ext2)." El nombre del tipo de archivo debe ser el nombre del tipo de archivo registrado, que puede ver en el elemento del panel de control Opciones de carpeta. Ejemplo: "Documento HTML ( \*.htm; \*.html)."
    -   **Excepción:** En el caso de los meta-filtros, quite la lista de extensiones de archivo para eliminar el desorden. Ejemplos: "Todos los archivos", "Todas las imágenes", "Toda la música" y "Todos los vídeos".
-   Use [mayúsculas de estilo oración](glossary.md) para los nombres de tipo de archivo y minúsculas para las extensiones de tipo de archivo.

### <a name="open-folder"></a>Abrir carpeta

-   **Para los nuevos programas, use el cuadro de diálogo Abrir archivos en el modo "seleccionar carpetas".** Para ello, se requiere Windows Vista o posterior, por lo que debe usar el cuadro de diálogo Abrir carpeta para los programas que se ejecutan en versiones anteriores de Windows.
    -   **Desarrolladores:** Puede usar el cuadro de diálogo Abrir archivos en el modo "seleccionar carpetas" mediante la marca \_ PICKFOLDERS de FOS.

### <a name="font"></a>Fuente

-   Si es necesario, puede filtrar la lista de fuentes para mostrar solo las fuentes disponibles para el programa.

### <a name="persistence"></a>Persistencia

-   Considere la posibilidad de hacer que los siguientes valores sea persistentes para usarlos como valores predeterminados posteriores:
    -   Valores de entrada (ejemplos: carpetas predeterminadas, nombres de archivo predeterminados).
    -   Opciones seleccionadas (ejemplos: impresora seleccionada, opciones de impresión).
    -   Vistas (ejemplos: mostrar imágenes en vista en miniatura, mostrar imágenes sin nombres de archivo, ordenar por fecha, anchos de columna).
    -   Presentación (ejemplos: tamaño de la ventana, ubicación y contenido).

**Excepción:** No haga que estos valores se conserven para los diálogos comunes cuando su uso sea tal que es mucho más probable que los usuarios quieran volver a empezar por completo.

-   Al determinar los valores predeterminados, tenga en cuenta qué usuarios de destino es más probable que quieran en función de los escenarios importantes. Además, considere escenarios dentro de una instancia de programa, en varias instancias (consecutivas o simultáneas) y en varios documentos. No haga que los valores se conserven en circunstancias que probablemente no sean útiles.
    -   **Ejemplo:** Para una aplicación típica basada en documentos, resulta útil usar la configuración persistente de Abrir archivo y Guardar archivo dentro de una instancia de programa y entre instancias consecutivas, pero mantener las instancias simultáneas independientes. De este modo, los usuarios pueden trabajar de forma eficaz con varios documentos a la vez.
-   Haga que la configuración se conserve por programa y por usuario.

 

