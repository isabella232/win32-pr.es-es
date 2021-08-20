---
title: Ventajas de usar SIS
description: Las ventajas de usar SIS y la arquitectura de copia de seguridad de SIS son las siguientes.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Copia de seguridad del almacén de instancia única (SIS), ventajas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc27eeefe8aa9a61566ea0a1d1e8fd1eca6c718c594ebf232572f16c44e3f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173969"
---
# <a name="advantages-of-using-sis"></a>Ventajas de usar SIS

Las ventajas de usar SIS y la arquitectura de copia de seguridad de SIS son las siguientes:

-   La arquitectura de SIS mantiene automáticamente las conexiones entre los vínculos de SIS y los archivos de respaldo a medida que las aplicaciones de copia de seguridad llaman a las funciones de la API de copia de seguridad de SIS.
-   El contenido de los puntos de reanados de SIS es opaco para las aplicaciones de copia de seguridad y restauración, lo que garantiza que las actualizaciones a los componentes internos del SIS no requieran un cambio en la API de SIS ni en las aplicaciones de copia de seguridad y restauración que llaman a las funciones de la API de SIS. Solo necesita volver a compilar la aplicación con una nueva versión de la DLL de SIS, denominada Sisbkup.dll.
-   Dado que SIS se implementa como controlador de filtro del sistema de archivos, realiza un seguimiento constante de las conexiones entre los vínculos de SIS y los archivos de respaldo. Cuando se hace una copia de seguridad de los archivos y se restauran, la copia de seguridad de SIS garantiza que solo se realizará una copia de seguridad y restauración de una instancia del archivo de copia de seguridad, independientemente del número de vínculos de SIS que apunten a él.

 

 




