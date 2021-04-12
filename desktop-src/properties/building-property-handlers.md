---
description: En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277823"
---
# <a name="implementing-property-handlers"></a>Implementar controladores de propiedades

En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos. Para habilitar un sistema en el que se puedan buscar elementos en función de sus metadatos y de que los usuarios puedan leer o escribir esos metadatos, Windows Vista presentó un nuevo sistema de propiedades. Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades. En este conjunto de temas se describe cómo se puede crear un controlador que lea y escriba propiedades en una secuencia de archivo. Estos controladores se denominan controladores de propiedades y cada uno está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo.

En los temas siguientes se describen los requisitos y las estrategias que conlleva la definición de las propiedades y los controladores de propiedades.

-   [Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
-   [Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
-   [Usar listas de propiedades](./building-property-handlers-property-lists.md)
-   [Inicializar controladores de propiedades](./building-property-handlers-property-handlers.md)
-   [Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
-   [Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear propiedades personalizadas.](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descripción de propiedad](./propdesc-schema-entry.md)
</dt> </dl>

 

 
