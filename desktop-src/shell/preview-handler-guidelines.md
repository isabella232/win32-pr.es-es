---
description: Cuando se proporciona una vista previa, deben seguirse las siguientes directrices.
title: Instrucciones de controlador de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910770"
---
# <a name="preview-handler-guidelines"></a>Instrucciones de controlador de vista previa

Cuando se proporciona una vista previa, deben seguirse las siguientes directrices.

-   Una vista previa debe contener una interfaz de usuario mínima; es simplemente una vista previa. Debería mostrar solo el contenido del archivo. No debe mostrar cuadros de diálogo, pantallas de presentación, barras de herramientas o paneles de tareas. El panel de lectura se usará normalmente junto con la búsqueda para identificar rápidamente un archivo. Cualquier cosa que esté abarrotando el panel de lectura o que, de otro modo, se destrae del contenido del archivo o provoca retrasos en la presentación de la vista previa debe evitarse.
-   La vista previa debe permitir al usuario navegar por el documento. El usuario también debe poder seleccionar y copiar texto.
-   La vista previa no debe consumir mucha memoria, debe consumir recursos mínimos y debe tener un tiempo de inicio rápido.
-   Se debe bloquear la ejecución de todos los scripts y macros del archivo en el que se va a obtener una vista previa para la seguridad y la privacidad.
-   La vista previa debe admitir aceleradores de teclado para la navegación y la selección que admite la aplicación. También debe mostrar un menú contextual al hacer clic con el botón secundario.
-   Cuando un archivo se muestra como una vista previa, la vista previa no debe bloquear el archivo. Se puede obtener una vista previa de un archivo y abrirlo en la aplicación asociada al mismo tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de vista previa y host de vista previa de Shell](preview-handlers.md)
</dt> <dt>

[Crear controladores de vista previa](building-preview-handlers.md)
</dt> </dl>

 

 



