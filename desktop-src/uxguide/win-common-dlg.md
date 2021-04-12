---
title: Cuadros de diálogo comunes
description: Los cuadros de diálogo comunes de Microsoft Windows se componen de los cuadros de diálogo Abrir archivo, guardar archivo, abrir carpeta, buscar y reemplazar, imprimir, configurar página, fuente y color.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 336cb368fa25bf68313e2bf336de68845a87e663
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104424108"
---
# <a name="common-dialogs"></a>Cuadros de diálogo comunes

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los cuadros de diálogo comunes de Microsoft Windows se componen de los cuadros de diálogo Abrir archivo, guardar archivo, abrir carpeta, buscar y reemplazar, imprimir, configurar página, fuente y color.

## <a name="open-file"></a>Abrir archivo

![captura de pantalla del cuadro de diálogo abrir ](images/win-common-dlg-image1.png)

Open File está optimizado para buscar rápidamente los elementos que se van a usar con un programa.

## <a name="save-file"></a>Guardar archivo

![captura de pantalla del cuadro de diálogo Guardar como ](images/win-common-dlg-image2.png)

Guardar archivo cierra el bucle guardando un archivo con sus metadatos.

## <a name="open-folder"></a>Abrir carpeta

![captura de pantalla del cuadro de diálogo Buscar archivos o carpetas ](images/win-common-dlg-image3.png)

Abrir carpeta es específicamente para elegir carpetas.

## <a name="find-and-replace"></a>Buscar y reemplazar

![captura de pantalla de los cuadros de diálogo Buscar y reemplazar ](images/win-common-dlg-image4.png)

Buscar permite a los usuarios buscar cadenas de texto, mientras que la opción reemplazar versión permite a los usuarios reemplazar las coincidencias por otra cadena.

## <a name="print"></a>Impresión

![captura de pantalla del cuadro de diálogo Imprimir ](images/win-common-dlg-image5.png)

Imprimir permite a los usuarios seleccionar lo que se va a imprimir, el número de copias que se van a imprimir y la secuencia de intercalación, junto con la capacidad de elegir y configurar las impresoras.

## <a name="page-setup"></a>Configurar página

![captura de pantalla del cuadro de diálogo Configurar página ](images/win-common-dlg-image6.png)

Configurar página permite a los usuarios seleccionar el tamaño y el origen del papel, la orientación de la página y los márgenes.

## <a name="font"></a>Fuente

![captura de pantalla del cuadro de diálogo fuente ](images/win-common-dlg-image7.png)

Fuente muestra las fuentes y los tamaños de punto de las fuentes instaladas disponibles.

## <a name="color"></a>Color

![captura de pantalla del cuadro de diálogo Editar colores ](images/win-common-dlg-image8.png)

Color permite a los usuarios seleccionar un color, ya sea a través de un conjunto predefinido de colores o eligiendo un color "personalizado".

## <a name="design-concepts"></a>Conceptos de diseño

Mediante el uso de los cuadros de diálogo comunes, puede proporcionar a los usuarios una experiencia coherente en distintos programas. Además, mediante el uso de cuadros de diálogo comunes, también puede ayudar a los usuarios a ofrecer una experiencia eficaz y agradable.

Puede mejorar significativamente la experiencia de los usuarios con estos cuadros de diálogo eligiendo los valores predeterminados más apropiados para:

-   Valores de entrada (ejemplos: carpetas predeterminadas, nombres de archivo predeterminados).
-   Opciones seleccionadas (ejemplos: impresora seleccionada, opciones de impresión).
-   Vistas (ejemplos: mostrar imágenes en la vista en miniatura, mostrar imágenes sin nombres de archivo, ordenar por fecha, anchos de columna).
-   Presentación (ejemplos: tamaño, ubicación y contenido de la ventana).

Debe determinar los valores predeterminados iniciales y los valores predeterminados posteriores. Los valores predeterminados iniciales vienen determinados por el programa y según el uso esperado del usuario de destino, mientras que los valores predeterminados posteriores se basan en el uso real. El uso pasado es el mejor indicador del uso futuro.

¿Son eficientes los valores predeterminados del programa? Supervise el número de pasos que los usuarios deben llevar a cabo para realizar las tareas más comunes. Si los usuarios tienen que repetir los mismos pasos potencialmente innecesarios cada vez que realizan una tarea, se pueden mejorar los valores predeterminados.

**Si solo hace algo...**

Ofrezca a los usuarios una experiencia eficaz y agradable seleccionando los valores predeterminados iniciales y posteriores.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

**?! Use los cuadros de diálogo comunes para obtener una experiencia de usuario coherente. No cree las suyas propias.** Es especialmente difícil crear interfaces de IU personalizadas que naveguen por el espacio de nombres correctamente y de forma segura. Tenga en cuenta que puede personalizar los cuadros de diálogo comunes si es necesario.

En Windows Vista, el archivo Open y el archivo Save tienen una nueva arquitectura extensible para facilitar la exposición de funcionalidad adicional. Este mecanismo es lo suficientemente flexible como para cumplir los requisitos mínimos de los principales proveedores de software independientes (ISV), pero no se interrumpirá en las futuras versiones de Windows.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   Cuando sea necesario, proporcione alternativas más directas o no [modales](glossary.md) . Permitir a los usuarios:
    -   Abra los archivos colocándolos en el programa.
    -   Guarde los archivos con el nombre y la ubicación actuales con un comando Guardar.
    -   Busque la siguiente repetición de una cadena mediante la tecla F3.
    -   Imprimir una copia de un documento completo en la impresora predeterminada con un comando imprimir.
    -   Cambiar fuentes y atributos de fuente mediante una barra de herramientas o una ventana de paleta.
    -   Cambiar los colores mediante una barra de herramientas o una ventana de paleta.
-   Use los siguientes comandos para mostrar cuadros de diálogo comunes (proporcionados junto con sus [claves de acceso](glossary.md)preferidas):



|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Cuadro de diálogo común**<br/> | **Comando**<br/>                        |
| Abrir archivo<br/>         | Abrir...<br/>                            |
| Guardar archivo<br/>         | Guardar como...<br/>                         |
| Abrir carpeta<br/>       | Abrir carpeta... o elija carpeta...<br/> |
| Buscar y reemplazar<br/>  | Buscar... o reemplazar...<br/>              |
| Impresión<br/>             | Imprimir...<br/>                           |
| Configurar página<br/>        | Configurar página...<br/>                      |
| Fuente<br/>              | Fuente... o elija fuente...<br/>          |
| Color<br/>             | Color... o elija color...<br/>        |



 

-   Puede usar comandos más específicos, según corresponda. Ejemplo: para exportar un archivo, use el comando Exportar archivo en lugar de guardar como.
-   Establezca el título del cuadro de diálogo para que refleje el comando que lo inició. Ejemplo: si se inicia Save file desde un comando export File, cambie el nombre del cuadro de diálogo a Export File.

### <a name="open-file"></a>Abrir archivo

-   En la carpeta predeterminada inicial, use una carpeta especializada (imágenes, música, vídeos) según corresponda; de lo contrario, use documentos.
-   En el caso de las carpetas predeterminadas posteriores, use la última carpeta abierta por el usuario mediante el programa.
-   Al abrir archivos fotográficos, suprima los nombres de archivo de forma predeterminada. Las fotos normalmente se identifican por sus miniaturas y sus nombres normalmente no son significativos.

### <a name="save-file"></a>Guardar archivo

-   Para la carpeta predeterminada inicial (si se está guardando un archivo nuevo por primera vez), use la carpeta especializada (imágenes, música, vídeos) según corresponda; de lo contrario, use documentos.
-   En el caso de los archivos temporales, utilice la carpeta temporal del usuario actual. Elija sencillo, pero nombres de archivo únicos. Ejemplo: Use File0001. tmp en lugar de ~ DF1A92. tmp.
    -   **Desarrolladores:** Puede obtener la carpeta temporal del usuario actual mediante la función de la API de GetTempPath.
-   Para el nombre de archivo predeterminado inicial, use un nombre predeterminado único basado en:
    -   El contenido del archivo, si se conoce. Ejemplo: las primeras palabras de un documento.
    -   Patrón elegido por el usuario. Ejemplo: Si el archivo anterior se llamaba "Hawai 1.jpg", elija "Hawai 2.jpg" como el siguiente archivo.
    -   Modelo genérico basado en el tipo de archivo. Ejemplo: "Photo1.jpg".
-   En el caso de los valores predeterminados posteriores (si el archivo ya existe), use la carpeta y el nombre actuales del archivo.
-   Al guardar un archivo, conserve su fecha de creación. Si el programa guarda archivos mediante la creación de un archivo temporal, elimina el original y cambia el nombre del archivo temporal por el original, asegúrese de copiar la fecha de creación del archivo original.
-   Use guardar archivo si el usuario selecciona el comando Guardar sin especificar un nombre de archivo.

### <a name="file-types-lists"></a>Listas de tipos de archivo

**Nota:** Las listas de tipos de archivo se usan en el archivo Open y en el archivo Save para determinar los tipos de archivos que se muestran y la extensión de archivo predeterminada.

-   Si la lista de tipos de archivo es breve (cinco o menos), ordene la lista por probabilidad de uso. Si la lista es larga (seis o más), use un orden alfabético para facilitar la búsqueda de los tipos.
-   En guardar archivo, incluya todas las variaciones de las extensiones de archivo admitidas, incluso si es poco frecuente, y ponga primero la extensión más común. La lógica de control de archivos examina esta lista para determinar si el usuario proporcionó una extensión de archivo compatible. Ejemplo: Si una lista de tipos de archivo JPEG solo incluye. jpg y. JPEG, el archivo test. jpe podría guardarse como test.jpe.jpg.
-   En el caso de Save File, el tipo de archivo predeterminado inicial es el más probable por el usuario de destino. El siguiente valor predeterminado es el tipo actual del archivo.
-   En el caso de Open File, el tipo de archivo predeterminado inicial es el más probable por el usuario de destino. El siguiente valor predeterminado debe ser el último tipo de archivo utilizado.
-   Para abrir archivo, incluya una entrada "todos los archivos" como primer elemento si los usuarios pueden abrir cualquier tipo de archivo o si necesita ver todos los archivos de una carpeta al mismo tiempo. Considere la posibilidad de proporcionar otros filtros de metadatos, como "todas las imágenes", "toda la música" y "todos los vídeos". Colóquelos inmediatamente después de "todos los archivos".
-   Use el formato "nombre de tipo de archivo ( \* . EXT1; \* . ext2) ". El nombre del tipo de archivo debe ser el nombre del tipo de archivo registrado, que se puede ver en el elemento del panel de control opciones de carpeta. Ejemplo: "documento HTML ( \* . htm; \* . HTML) ".
    -   **Excepción:** En el caso de los metafiltros, quite la lista de extensiones de archivo para eliminar la confusión. Ejemplos: "todos los archivos", "todas las imágenes", "toda la música" y "todos los vídeos".
-   Use [mayúsculas](glossary.md) y minúsculas para los nombres de tipo de archivo y en minúsculas para las extensiones de tipo de archivo.

### <a name="open-folder"></a>Abrir carpeta

-   **En el caso de los nuevos programas, use el cuadro de diálogo abrir archivos del modo "seleccionar carpetas".** Esto requiere Windows Vista o posterior, por lo que debe usar el cuadro de diálogo Abrir carpeta para los programas que se ejecutan en versiones anteriores de Windows.
    -   **Desarrolladores:** Puede usar el cuadro de diálogo abrir archivos del modo "seleccionar carpetas" mediante el uso de la marca de FOS \_ PICKFOLDERS.

### <a name="font"></a>Fuente

-   Si es necesario, puede filtrar la lista fuente para mostrar solo las fuentes disponibles para el programa.

### <a name="persistence"></a>Persistencia

-   Considere la posibilidad de hacer que los valores siguientes sean persistentes para su uso como valores predeterminados posteriores:
    -   Valores de entrada (ejemplos: carpetas predeterminadas, nombres de archivo predeterminados).
    -   Opciones seleccionadas (ejemplos: impresora seleccionada, opciones de impresión).
    -   Vistas (ejemplos: mostrar imágenes en la vista en miniatura, mostrar imágenes sin nombres de archivo, ordenar por fecha, anchos de columna).
    -   Presentación (ejemplos: tamaño, ubicación y contenido de la ventana).

**Excepción:** No haga que estos valores se conserven en cuadros de diálogo comunes cuando su uso sea tal que los usuarios tengan mucho más probabilidades de comenzar a usarse por completo.

-   Al determinar los valores predeterminados, considere qué usuarios de destino es más probable que deseen en función de los escenarios importantes. Además, considere escenarios dentro de una instancia de programa, en varias instancias (consecutivas o simultáneas) y en varios documentos. No haga que los valores se conserven en circunstancias que probablemente no sean útiles.
    -   **Ejemplo:** En el caso de las aplicaciones típicas basadas en documentos, resulta útil usar archivos abiertos persistentes y guardar valores de archivo dentro de una instancia del programa y en instancias consecutivas, pero mantener independientes las instancias simultáneas. De este modo, los usuarios pueden trabajar de forma eficaz con varios documentos a la vez.
-   Haga que la configuración se mantenga en cada programa y por usuario.

 

