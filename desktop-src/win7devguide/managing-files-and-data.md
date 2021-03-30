---
title: Administrar archivos y datos
description: Los usuarios tienen un acceso más sencillo a los archivos y datos en Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995409"
---
# <a name="managing-files-and-data"></a>Administrar archivos y datos

Los usuarios tienen un acceso más sencillo a los archivos y datos en Windows 7. Las nuevas API hacen que los archivos y las vistas sean más informativos, lo que permite a las aplicaciones ofrecer información relevante e distintiva al explorador de Windows. Además, las aplicaciones se benefician del nuevo modelo de *bibliotecas* , una noción útil y más abstracta del espacio de almacenamiento de usuario que las carpetas, y también pueden participar en bibliotecas comunes de tipos de archivo similares compartidos por aplicaciones diferentes.

## <a name="libraries"></a>Bibliotecas

Windows 7 presenta el concepto de *bibliotecas* como destinos en los que los desarrolladores y los usuarios finales pueden buscar y organizar sus datos como colecciones de elementos que pueden abarcar varias ubicaciones en el equipo local, así como en equipos remotos.

Las API de *biblioteca* proporcionan a los desarrolladores una forma sencilla de crear aplicaciones que crean, interactúan con las bibliotecas y admiten *bibliotecas* como elementos de primera clase dentro de las aplicaciones. Las *bibliotecas* también se pueden seleccionar mediante el cuadro de diálogo Selector de carpetas. Las aplicaciones pueden enumerar ámbitos de biblioteca relevantes o pueden utilizar la biblioteca directamente como una carpeta. (Consulte [bibliotecas de Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) y [bibliotecas de Windows 7: recursos para desarrolladores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).

![Biblioteca de imágenes de Windows 7](images/windows7-10.jpg)

La *biblioteca de imágenes* muestra las imágenes independientemente de dónde estén almacenadas

## <a name="file-formats-and-data-stores"></a>Formatos de archivo y almacenes de datos

En Windows 7, el explorador de Windows facilita la administración de archivos y la manipulación para el usuario de varias maneras:

-   La vista previa del tipo de archivo de la aplicación es más accesible con un botón nuevo que permite a los usuarios mostrar y ocultar el panel de vista previa.
-   Las pilas visuales envolventes agregan imágenes en miniatura para los tipos de archivo en una vista.
-   Las vistas del explorador de Windows muestran información útil basada en las propiedades escritas con el controlador de propiedad.
-   Fragmentos de código de documento y resaltado de referencias use la implementación de la interfaz de **IFilter** para facilitar la búsqueda y la búsqueda de archivos.
-   Los comandos y verbos de menú contextual son más fáciles de implementar.

Al implementar todos los controladores de formato adecuados para los elementos devueltos por el controlador de protocolo, los resultados de la búsqueda del almacén de datos personalizado pueden ser tan completos como los resultados de la búsqueda de archivos. Las *bibliotecas* se crean automáticamente para los controladores de protocolo, por lo que los usuarios pueden limitar sus búsquedas fácilmente. Y la lógica para crear *bibliotecas* se puede personalizar fácilmente a través del registro. (Consulte [desarrollo de filtros para Windows Search](../search/-search-3x-wds-extidx-filters.md)).

![Biblioteca de documentos de Windows 7](images/windows7-11.jpg)

En Windows 7, el explorador de Windows facilita la administración y manipulación de archivos

 

 