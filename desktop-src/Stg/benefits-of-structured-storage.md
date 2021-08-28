---
title: Ventajas de structured Storage
description: COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Structured Storage Strctd Stg , ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a52159f37b3bf443419beaadbcf9f76aa9c5d7209e04b25506eea850c4d3d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663583"
---
# <a name="benefits-of-structured-storage"></a>Ventajas de structured Storage

COM proporciona un conjunto de servicios denominados colectivamente almacenamiento estructurado. Entre las ventajas de estos servicios se encuentra la reducción de las penalizaciones de rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un archivo plano. En lugar de un archivo plano, COM almacena los objetos independientes en un único archivo estructurado que consta de dos elementos principales: objetos de almacenamiento y objetos de secuencia. Juntos, funcionan como un sistema de archivos dentro de un archivo.

El almacenamiento estructurado resuelve problemas de rendimiento al eliminar la necesidad de reescribir completamente un archivo en el almacenamiento cada vez que se agrega un nuevo objeto a un archivo compuesto o un objeto existente aumenta de tamaño. Los nuevos datos se escriben en la siguiente ubicación disponible en el almacenamiento permanente y el objeto de almacenamiento actualiza la tabla de punteros que mantiene para realizar un seguimiento de las ubicaciones de sus objetos de almacenamiento y objetos de secuencia. Al mismo tiempo, el almacenamiento estructurado permite a los usuarios finales interactuar y administrar un archivo compuesto como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.

El almacenamiento estructurado también tiene otras ventajas:

-   **Acceso incremental.** Si un usuario necesita acceder a un objeto dentro de un archivo compuesto, el usuario puede cargar y guardar solo ese objeto, en lugar de todo el archivo.
-   **Uso múltiple de**. Más de un usuario final o aplicación pueden leer y escribir simultáneamente información en el mismo archivo compuesto.
-   **Procesamiento de transacciones.** Los usuarios pueden leer o escribir en archivos compuestos COM en modo de transacción, donde los cambios realizados en el archivo se almacena en búfer y, posteriormente, se pueden realizar confirmaciones en el archivo o invertirse.
-   **La memoria baja guarda**. El almacenamiento estructurado proporciona facilidades para guardar archivos en situaciones de memoria baja.

 

 




