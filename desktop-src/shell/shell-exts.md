---
description: En este conjunto de temas se describe cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Trabajar con extensiones de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804b121ccf633b44574ae956b367143eebdaf7a2a3a8a9cc8400995522b4cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452861"
---
# <a name="working-with-shell-extensions"></a>Trabajar con extensiones de shell

Las funcionalidades del Shell se pueden ampliar con entradas del Registro y .ini archivos. Aunque este enfoque para extender el shell es sencillo y adecuado para muchos propósitos, es limitado. Por ejemplo, si usa el Registro para especificar un icono personalizado para un tipo de archivo, aparecerá el mismo icono para cada archivo de ese tipo. La extensión del Shell con el Registro no permite variar el icono de los distintos miembros del tipo de archivo. Otros aspectos del Shell,  como la hoja de propiedades Propiedades que se puede mostrar cuando se hace clic con el botón derecho en un archivo, no se pueden modificar en absoluto con el Registro.

Un enfoque más eficaz y flexible para extender el shell es implementar controladores *de extensión de shell*. Estos controladores se pueden implementar para diversas acciones que el Shell puede realizar. Antes de realizar la acción, el Shell consulta el controlador de extensión, lo que le ofrece la oportunidad de modificar la acción. Un ejemplo común es un controlador de extensión de menú contextual. Si se implementa uno para un tipo de archivo, se consultará cada vez que se haga clic con el botón derecho en uno de los archivos. A continuación, el controlador puede especificar elementos de menú adicionales en función de archivo por archivo, en lugar de tener el mismo conjunto para todos los archivos de ese tipo de archivo.

En este conjunto de temas se describe cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell. Los siguientes controladores están asociados a un tipo de archivo determinado y permiten especificar archivos por archivo.



| Controlador                                               | Descripción                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de menú contextual](context-menu-handlers.md)    | Se llama antes de que se muestre el menú contextual de un archivo. Permite agregar elementos al menú contextual archivo por archivo.                                               |
| [Controlador de datos](how-to-create-data-handlers.md)       | Se llama cuando se realiza una operación de arrastrar y colocar en objetos de Shell. Permite proporcionar formatos de Portapapeles adicionales al destino de colocación.                            |
| [Controlador de colocación](how-to-create-drop-handlers.md)       | Se llama cuando se arrastra o se descarta un objeto de datos en un archivo. Permite convertir un archivo en un destino de colocación.                                                          |
| [Controlador de iconos](how-to-create-icon-handlers.md)       | Se llama antes de que se muestre el icono de un archivo. Le permite reemplazar el icono predeterminado del archivo por un icono personalizado en función de archivo por archivo.                                    |
| [Controlador de la hoja de propiedades](propsheet-handlers.md)      | Se llama antes de que se muestre **la hoja de** propiedades Propiedades de un objeto. Permite agregar o reemplazar páginas.                                                              |
| [**Controlador de imágenes en miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Proporciona una imagen para representar el elemento.                                                                                                                                   |
| [**Controlador de recuadro informativo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre el objeto.                                                                                               |
| [**Controlador de metadatos**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Proporciona acceso de lectura y escritura a los metadatos (propiedades) almacenados en un archivo. Se puede usar para ampliar la vista Detalles, la información sobre información, la página de propiedades y las características de agrupación. |



 

Otros no están asociados a un tipo de archivo determinado, pero se llama a ellos antes de algunas operaciones de Shell.



| Controlador                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de columnas](../lwef/column-handlers.md)                             | Lo llama Windows Explorer antes de mostrar la vista Detalles de una carpeta. Permite agregar columnas personalizadas a la vista Detalles.        |
| [Controlador de enlace de copia](how-to-create-copy-hook-handlers.md)          | Se llama cuando se va a mover, copiar, eliminar o cambiar el nombre de una carpeta o un objeto de impresora. Permite aprobar o vetar la operación.   |
| [Controlador de arrastrar y colocar](context-menu-handlers.md)                 | Se llama cuando se arrastra un archivo con el botón derecho del mouse. Permite modificar el menú contextual que se muestra.                     |
| [Controlador de superposición de iconos](how-to-implement-icon-overlay-handlers.md) | Se llama antes de que se muestre el icono de un archivo. Permite especificar una superposición para el icono del archivo.                                          |
| [Controlador de búsqueda](../lwef/search-handlers.md)                             | Se llama para iniciar un motor de búsqueda. Permite implementar un motor de búsqueda personalizado accesible desde el **menú** Inicio o Windows Explorer. |



 

Los detalles de cómo implementar controladores de extensión específicos se tratan en las secciones enumeradas anteriormente. Para obtener información sobre los problemas de implementación que son comunes a todos los controladores de extensión de Shell, consulte estos temas:

-   [Inicialización de controladores de extensión de shell](int-shell-exts.md)
-   [Registro de controladores de extensión de shell](reg-shell-exts.md)

 

 
