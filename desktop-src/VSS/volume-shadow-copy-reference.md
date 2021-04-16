---
description: El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad de volumen mientras las aplicaciones del sistema (denominadas escritores) continúan escribiendo en los volúmenes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referencia de la API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541750"
---
# <a name="volume-shadow-copy-api-reference"></a>Referencia de la API de instantáneas de volumen

El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad de volumen mientras las aplicaciones del sistema (denominadas escritores) continúan escribiendo en los volúmenes.

VSS admite estas copias de seguridad a través de la creación de instantáneas, un duplicado del volumen original en un momento dado.

Los desarrolladores de terceros pueden usar la API de VSS para crear solicitantes (por ejemplo, una aplicación de copia de seguridad) para crear y administrar instantáneas.

Las aplicaciones de nivel de sistema conocidas como proveedores llevan a cabo el trabajo real de creación y representación de las instantáneas.

Los desarrolladores también pueden usar la API para construir escritores: aplicaciones compatibles con VSS que pueden coordinar las operaciones de e/s con la creación y manipulación de instantáneas.

-   [Clases de API de instantáneas de volumen](volume-shadow-copy-api-classes.md)
-   [Tipos de datos de la API de instantáneas de volumen](volume-shadow-copy-api-data-types.md)
-   [Enumeraciones de la API de instantáneas de volumen](volume-shadow-copy-api-enumeration-types.md)
-   [Funciones de la API de instantáneas de volumen](volume-shadow-copy-api-functions.md)
-   [Interfaces de la API de instantáneas de volumen](volume-shadow-copy-api-interfaces.md)
-   [Estructuras de API de instantáneas de volumen](volume-shadow-copy-api-structures.md)
-   [Glosario de instantáneas de volumen](volume-shadow-copy-glossary.md)

Para obtener más información sobre la escritura de solicitantes y escritores, vea [usar el servicio de instantáneas de volumen](using-the-volume-shadow-copy-service.md).

 

 



