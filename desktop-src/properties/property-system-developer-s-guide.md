---
description: En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos.
ms.assetid: 3281736b-f9ea-4699-a128-3bce6810126e
title: Guía del desarrollador del sistema de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6746c24d24a6926d20078c00f6780c72fb7c8e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667651"
---
# <a name="property-system-developers-guide"></a>Guía del desarrollador del sistema de propiedades

En Windows Vista y versiones posteriores, los metadatos se convierten en centrales como un método para organizar elementos como archivos, correo electrónico o contactos. Para habilitar un sistema en el que se puedan buscar elementos en función de sus metadatos y de que los usuarios puedan leer o escribir esos metadatos, Windows Vista presentó un nuevo sistema de propiedades. Los metadatos de este sistema se representan mediante un conjunto extensible de propiedades. Con la introducción de propiedades en Windows Vista que abstraen las características específicas de los elementos, como fotos, música, documentos, mensajes, contactos y archivos, los fabricantes de software independientes (ISV) ahora pueden introducir sus propias propiedades en la plataforma si no hay ninguna propiedad existente que satisfaga sus necesidades.

En esta sección se describen los siguientes escenarios de desarrollo en el sistema de propiedades de Windows:

-   [Crear propiedades personalizadas.](./building-property-handlers-property-schemas.md)
-   [Implementar controladores de propiedades](./building-property-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general del sistema de propiedades](property-system-overview.md)
</dt> <dt>

[Referencia del sistema de propiedades](property-system-reference.md)
</dt> <dt>

[Ejemplos de código del sistema de propiedades](property-system-code-samples.md)
</dt> </dl>

 

 
