---
description: Obtenga información sobre cómo crear un controlador de propiedades que lee y escribe propiedades en y desde una secuencia de archivos. Cada controlador está asociado a un tipo de archivo determinado.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481840"
---
# <a name="implementing-property-handlers"></a>Implementar controladores de propiedades

En Windows Vista y versiones posteriores, los metadatos se convierten en fundamentales como método para organizar elementos como archivos, correo electrónico o contactos. Para habilitar un sistema en el que se pueden buscar elementos en función de sus metadatos y en el que los usuarios puedan leer o escribir los metadatos, Windows Vista introdujo un nuevo sistema de propiedades. Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades. En este conjunto de temas se describe cómo puede crear un controlador que lee y escribe propiedades en y desde una secuencia de archivos. Estos controladores se denominan controladores de propiedades y cada uno de ellos está asociado a tipos de archivo determinados, identificados por la extensión de nombre de archivo.

En los temas siguientes se tratan los requisitos y las estrategias implicados en la definición de las propiedades y los controladores de propiedades.

-   [Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
-   [Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
-   [Usar listas de propiedades](./building-property-handlers-property-lists.md)
-   [Inicialización de controladores de propiedades](./building-property-handlers-property-handlers.md)
-   [Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
-   [Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear propiedades personalizadas.](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descripción de propiedad](./propdesc-schema-entry.md)
</dt> </dl>

 

 
