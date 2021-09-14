---
title: Administración de archivos y datos
description: Los usuarios tienen un acceso más sencillo a los archivos y los datos Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251757"
---
# <a name="managing-files-and-data"></a>Administración de archivos y datos

Los usuarios tienen un acceso más sencillo a los archivos y los datos Windows 7. Las nuevas API hacen que los archivos y vistas sean más informativos, lo que permite que las aplicaciones proporcionen información relevante y distintiva a Windows Explorer. Además, las aplicaciones se benefician del nuevo modelo *de bibliotecas,* una noción útil y más abstracta de espacio de almacenamiento de usuario que las carpetas, y también pueden participar en bibliotecas comunes de tipos de archivo similares que comparten distintas aplicaciones.

## <a name="libraries"></a>Bibliotecas

Windows 7 presenta el concepto de bibliotecas como *destinos* donde los desarrolladores y los usuarios finales pueden encontrar y organizar sus datos como colecciones de elementos que pueden abarcar varias ubicaciones en el equipo local, así como en equipos remotos.

Las *API* de biblioteca proporcionan una manera sencilla para que los desarrolladores creen aplicaciones que creen, interactúen y admitan *bibliotecas* como elementos de primera clase dentro de las aplicaciones. *Las bibliotecas* también se pueden seleccionar mediante el cuadro de diálogo selector de carpetas. Las aplicaciones pueden enumerar los ámbitos de biblioteca pertinentes o pueden usar la biblioteca directamente como una carpeta. (Vea [bibliotecas Windows bibliotecas](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) y [Windows 7 Bibliotecas: recursos para desarrolladores).](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)

![Biblioteca de imágenes de Windows 7](images/windows7-10.jpg)

*La biblioteca de* imágenes muestra las imágenes independientemente de dónde se almacenen.

## <a name="file-formats-and-data-stores"></a>Formatos de archivo y almacenes de datos

En Windows 7, Windows Explorer facilita la administración y manipulación de archivos para el usuario de varias maneras:

-   La versión preliminar del tipo de archivo de la aplicación es más accesible con un nuevo botón que permite a los usuarios mostrar y ocultar el panel de vista previa.
-   Las pilas visuales inmersivas agregan imágenes en miniatura para los tipos de archivo de una vista.
-   Windows Las vistas del explorador muestran información útil basada en las propiedades escritas con el controlador de propiedades.
-   Los fragmentos de código de documento y el resaltado de pulsaciones usan la implementación de **la interfaz IFilter** para facilitar la búsqueda y la búsqueda de archivos.
-   Los verbos y comandos del menú contextual son más fáciles de implementar que nunca.

Al implementar todos los controladores de formato adecuados para los elementos devueltos desde el controlador de protocolo, los resultados de búsqueda del almacén de datos personalizado pueden ser tan enriquecidos como los resultados de la búsqueda de archivos. *Las bibliotecas* se crean automáticamente para los controladores de protocolo para que los usuarios puedan establecer fácilmente el ámbito de sus búsquedas. Y la lógica para crear *bibliotecas* se puede personalizar fácilmente a través del Registro. (Vea [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md)[Desarrollo de filtros para Windows Search]).

![Biblioteca de documentos de Windows 7](images/windows7-11.jpg)

En Windows 7, Windows Explorer facilita la administración y manipulación de archivos

 

 