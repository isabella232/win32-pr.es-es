---
title: Ventajas del almacenamiento estructurado
description: COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strctd de almacenamiento estructurado STG, ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773746"
---
# <a name="benefits-of-structured-storage"></a>Ventajas del almacenamiento estructurado

COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado. Entre las ventajas de estos servicios se reduce la reducción del rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un archivo plano. En lugar de un archivo sin formato, COM almacena los objetos independientes en un único archivo estructurado que consta de dos elementos principales: objetos de almacenamiento y objetos de secuencia. Juntos, funcionan como un sistema de archivos dentro de un archivo.

El almacenamiento estructurado resuelve los problemas de rendimiento al eliminar la necesidad de reescribir completamente un archivo en el almacenamiento cada vez que se agrega un nuevo objeto a un archivo compuesto, o cuando un objeto existente aumenta de tamaño. Los nuevos datos se escriben en la siguiente ubicación disponible en el almacenamiento permanente y el objeto de almacenamiento actualiza la tabla de punteros que mantiene para realizar el seguimiento de las ubicaciones de sus objetos de almacenamiento y objetos de secuencia. Al mismo tiempo, el almacenamiento estructurado permite a los usuarios finales interactuar y administrar un archivo compuesto como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.

El almacenamiento estructurado también tiene otras ventajas:

-   **Acceso incremental**. Si un usuario necesita tener acceso a un objeto dentro de un archivo compuesto, el usuario puede cargar y guardar solo ese objeto, en lugar de todo el archivo.
-   **Uso múltiple**. Más de un usuario final o una aplicación pueden leer y escribir información simultáneamente en el mismo archivo compuesto.
-   **Procesamiento de transacciones**. Los usuarios pueden leer o escribir en archivos compuestos COM en modo de transacción, donde los cambios realizados en el archivo se almacenan en búfer y, posteriormente, pueden confirmarse en el archivo o invertirse.
-   **Ahorro de memoria insuficiente**. El almacenamiento estructurado proporciona funciones para guardar archivos en situaciones de memoria insuficiente.

 

 




