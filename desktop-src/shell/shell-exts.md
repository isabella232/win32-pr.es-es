---
description: En este conjunto de temas se explica cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Trabajar con extensiones de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb696f4536cdb0fb6869be073771d431bd8d2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985986"
---
# <a name="working-with-shell-extensions"></a>Trabajar con extensiones de Shell

Las capacidades del shell se pueden extender con las entradas del registro y los archivos. ini. Aunque este enfoque para extender el Shell es sencillo y adecuado para muchos propósitos, es limitado. Por ejemplo, si usa el registro para especificar un icono personalizado para un tipo de archivo, aparecerá el mismo icono para cada archivo de ese tipo. La extensión del shell con el registro no le permite modificar el icono de los distintos miembros del tipo de archivo. Otros aspectos del shell, como la hoja de propiedades **propiedades** que se pueden mostrar cuando se hace clic con el botón derecho en un archivo, no se pueden modificar en absoluto con el registro.

Un enfoque más eficaz y flexible para extender el Shell es implementar *controladores de extensión de Shell*. Estos controladores se pueden implementar para una serie de acciones que puede llevar a cabo el shell. Antes de realizar la acción, el shell consulta el controlador de extensión, lo que le otorga la oportunidad de modificar la acción. Un ejemplo común es un controlador de extensión de menú contextual. Si se implementa una para un tipo de archivo, se consultará cada vez que se haga clic con el botón derecho en uno de los archivos. A continuación, el controlador puede especificar elementos de menú adicionales cada archivo, en lugar de tener el mismo conjunto para todos los archivos de ese tipo de archivo.

En este conjunto de temas se explica cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell. Los siguientes controladores se asocian a un tipo de archivo determinado y permiten especificar cada archivo de forma individual.



| Controlador                                               | Descripción                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador del menú contextual](context-menu-handlers.md)    | Se llama antes de que se muestre el menú contextual de un archivo. Permite agregar elementos al menú contextual de forma individual para cada archivo.                                               |
| [Controlador de datos](how-to-create-data-handlers.md)       | Se le llama cuando se realiza una operación de arrastrar y colocar en objetos de Shell. Permite proporcionar formatos de Portapapeles adicionales al destino de colocación.                            |
| [Quitar controlador](how-to-create-drop-handlers.md)       | Se llama cuando se arrastra un objeto de datos o se coloca en un archivo. Permite crear un archivo en un destino de colocación.                                                          |
| [Controlador de iconos](how-to-create-icon-handlers.md)       | Se llama antes de que se muestre el icono de un archivo. Permite reemplazar el icono predeterminado del archivo con un icono personalizado en función de cada archivo.                                    |
| [Controlador de la hoja de propiedades](propsheet-handlers.md)      | Se llama antes de que se muestre la hoja de propiedades de **propiedades** de un objeto. Permite agregar o reemplazar páginas.                                                              |
| [**Controlador de imagen en miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Proporciona una imagen para representar el elemento.                                                                                                                                   |
| [**Controlador de recuadro informativo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre el objeto.                                                                                               |
| [**Controlador de metadatos**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Proporciona acceso de lectura y escritura a los metadatos (propiedades) almacenados en un archivo. Se puede usar para ampliar la vista de detalles, recuadros informativos, la página de propiedades y las características de agrupación. |



 

Otros no están asociados a un tipo de archivo determinado, pero se les llama antes que algunas operaciones de Shell.



| Controlador                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de columnas](../lwef/column-handlers.md)                             | Lo llama el explorador de Windows antes de mostrar la vista de detalles de una carpeta. Permite agregar columnas personalizadas a la vista de detalles.        |
| [Copiar controlador de enlace](how-to-create-copy-hook-handlers.md)          | Se llama cuando una carpeta o un objeto de impresora está a punto de moverse, copiarse, eliminarse o cambiarse de nombre. Permite aprobar o vetar la operación.   |
| [Controlador de arrastrar y colocar](context-menu-handlers.md)                 | Se le llama cuando se arrastra un archivo con el botón secundario del mouse. Permite modificar el menú contextual que se muestra.                     |
| [Controlador de superposición de iconos](how-to-implement-icon-overlay-handlers.md) | Se llama antes de que se muestre el icono de un archivo. Permite especificar una superposición para el icono del archivo.                                          |
| [Controlador de búsqueda](../lwef/search-handlers.md)                             | Se llama para iniciar un motor de búsqueda. Permite implementar un motor de búsqueda personalizado accesible desde el menú **Inicio** o el explorador de Windows. |



 

Los detalles sobre cómo implementar controladores de extensión específicos se tratan en las secciones anteriores. Para obtener una discusión de los problemas de implementación comunes a todos los controladores de extensión de Shell, vea estos temas:

-   [Inicializar controladores de extensión de Shell](int-shell-exts.md)
-   [Registrando controladores de extensión de Shell](reg-shell-exts.md)

 

 
