---
description: El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad del volumen mientras las aplicaciones del sistema (denominadas escritores) siguen escribiendo en los volúmenes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referencia de api de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751532"
---
# <a name="volume-shadow-copy-api-reference"></a>Referencia de api de instantáneas de volumen

El Servicio de instantáneas de volumen (VSS) es un conjunto de API de COM y C++ que permiten realizar copias de seguridad del volumen mientras las aplicaciones del sistema (denominadas escritores) siguen escribiendo en los volúmenes.

VSS admite estas copias de seguridad mediante la creación de instantáneas, un duplicado del volumen original en un momento dado.

Los desarrolladores de terceros pueden usar la API de VSS para crear solicitantes (como una aplicación de copia de seguridad) para crear y administrar instantáneas.

El trabajo real de crear y representar instantáneas se realiza mediante aplicaciones de nivel de sistema conocidas como proveedores.

Los desarrolladores también pueden usar la API para construir escritores: aplicaciones con vsS que pueden coordinar las operaciones de E/S con la creación y manipulación de instantáneas.

-   [Clases de API de instantáneas de volumen](volume-shadow-copy-api-classes.md)
-   [Tipos de datos de la API de instantáneas de volumen](volume-shadow-copy-api-data-types.md)
-   [Enumeraciones de api de instantáneas de volumen](volume-shadow-copy-api-enumeration-types.md)
-   [Funciones de la API de instantáneas de volumen](volume-shadow-copy-api-functions.md)
-   [Interfaces de api de instantáneas de volumen](volume-shadow-copy-api-interfaces.md)
-   [Estructuras de api de instantáneas de volumen](volume-shadow-copy-api-structures.md)
-   [Glosario de instantáneas de volumen](volume-shadow-copy-glossary.md)

Para obtener más información sobre cómo escribir solicitantes y escritores, vea [Using the Servicio de instantáneas de volumen](using-the-volume-shadow-copy-service.md).

 

 



