---
title: Operaciones de Access Control y de lectura
description: La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Access Control y leer operaciones de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075025"
---
# <a name="access-control-and-read-operations"></a>Operaciones de Access Control y de lectura

La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades. Si no tiene los derechos de acceso necesarios, se pueden producir errores en los intentos de enumeración de objetos o en propiedades de lectura con los siguientes códigos de error incluso si existe el objeto o la propiedad:

-   **E \_ ADS \_ \_ objeto de dominio no válido \_**
-   **\_no se \_ admite la propiedad de ADS \_ \_**
-   **\_ \_ \_ no \_ se encontró la propiedad de ADS**

Tenga en cuenta que un llamador **con \_ el derecho ADS \_ ACTRL \_ DS \_** acceso a un contenedor puede enumerar los objetos secundarios en el contenedor. Sin embargo, un intento de acceder a un objeto secundario puede seguir produciendo un error **como \_ E \_ ADS \_ objeto desconocido** si el autor de la llamada no tiene el **derecho de ADS \_ \_ ACTRL \_ DS \_ List \_ Object** Access al objeto secundario.

El impacto de la seguridad en las operaciones de lectura no se manifiesta necesariamente como un error. Por ejemplo, una operación de búsqueda puede realizarse correctamente, pero los resultados de la búsqueda no incluyen objetos o propiedades a los que el llamador no tiene acceso.

 

 




