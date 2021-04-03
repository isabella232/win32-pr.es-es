---
title: Ventajas del uso de SIS
description: Las ventajas de usar SIS y la arquitectura de copia de seguridad de SIS son las siguientes.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Copia de seguridad de almacenamiento de instancia única (SIS), ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075177"
---
# <a name="advantages-of-using-sis"></a>Ventajas del uso de SIS

Las ventajas de usar SIS y la arquitectura de copia de seguridad de SIS son las siguientes:

-   La arquitectura de SIS mantiene automáticamente las conexiones entre los vínculos de SIS y los archivos de copia de seguridad a medida que las aplicaciones de copia de seguridad llaman a las funciones de la API de copia de seguridad de SIS.
-   El contenido de los puntos de análisis de SIS es opaco para las aplicaciones de copia de seguridad y restauración, asegurándose de que las actualizaciones de los elementos internos de SIS no requieren un cambio en la API de SIS o en las aplicaciones de copia de seguridad y restauración que llaman a las funciones de la API de SIS. Solo necesita volver a compilar la aplicación con una nueva versión de la DLL de SIS, denominada Sisbkup.dll.
-   Dado que SIS se implementa como un controlador de filtro del sistema de archivos, realiza un seguimiento constante de las conexiones entre los vínculos de SIS y los archivos de copia de seguridad. Cuando se realiza una copia de seguridad y se restauran los archivos, la copia de seguridad de SIS garantiza que solo se realizará una copia de seguridad de una instancia del archivo de respaldo y se restaurará, independientemente del número de vínculos de SIS que lo señalen.

 

 




