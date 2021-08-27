---
description: Al proporcionar una versión preliminar, se deben seguir las siguientes directrices.
title: Instrucciones del controlador de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719633"
---
# <a name="preview-handler-guidelines"></a>Instrucciones del controlador de vista previa

Al proporcionar una versión preliminar, se deben seguir las siguientes directrices.

-   Una versión preliminar debe contener una interfaz de usuario mínima, simplemente una versión preliminar. Solo debe mostrar el contenido del archivo. No debe mostrar cuadros de diálogo, pantallas de presentación, barras de herramientas ni paneles de tareas. El panel de lectura se usará normalmente junto con la búsqueda para identificar rápidamente un archivo. Se debe evitar todo lo que abarrote el panel de lectura o que resta contenido del archivo o que provoca retrasos en la presentación en versión preliminar.
-   La versión preliminar debe permitir al usuario navegar por el documento. El usuario también debe poder seleccionar y copiar texto.
-   La versión preliminar no debe consumir mucha memoria, debe consumir recursos mínimos y debe tener un tiempo de inicio rápido.
-   Se debe bloquear la ejecución de todos los scripts y macros del archivo en versión preliminar por motivos de seguridad y privacidad.
-   La versión preliminar debe admitir aceleradores de teclado para la navegación y la selección, tal y como admite la aplicación. También debe mostrar un menú contextual cuando se hace clic con el botón derecho.
-   Cuando un archivo se muestra como una vista previa, la vista previa no debe bloquear el propio archivo. Un archivo se puede obtener una vista previa y abrirse en su aplicación asociada al mismo tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de vista previa y host de vista previa del shell](preview-handlers.md)
</dt> <dt>

[Compilar controladores de vista previa](building-preview-handlers.md)
</dt> </dl>

 

 



