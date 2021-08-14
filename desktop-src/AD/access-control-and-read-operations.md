---
title: Access Control y operaciones de lectura
description: La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Access Control operaciones de lectura y lectura de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f11dfd0b8d65bf0346f66fa4d7b959cb2893718bef44303d3774b19c29a97ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025505"
---
# <a name="access-control-and-read-operations"></a>Access Control y operaciones de lectura

La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades. Si no tiene los derechos de acceso necesarios, los intentos de enumerar objetos o leer propiedades pueden producir errores con los siguientes códigos de error, incluso pensando que el objeto o propiedad existe:

-   **E \_ ADS \_ INVALID \_ DOMAIN \_ OBJECT**
-   **NO \_ SE ADMITE LA PROPIEDAD E \_ \_ \_ ADS**
-   **E \_ ADS \_ PROPERTY \_ NOT \_ FOUND**

Tenga en cuenta que un llamador con acceso **\_ ADS RIGHT \_ ACTRL \_ DS \_ LIST** a un contenedor puede enumerar los objetos secundarios del contenedor. Pero un intento de acceder a un objeto secundario puede producir un error como **E \_ ADS UNKNOWN \_ \_ OBJECT** si el autor de la llamada no tiene acceso ADS **RIGHT \_ \_ ACTRL \_ DS LIST \_ \_ OBJECT** al objeto secundario.

El impacto de la seguridad en las operaciones de lectura no se manifiesta necesariamente como un error. Por ejemplo, una operación de búsqueda puede realizarse correctamente, pero los resultados de la búsqueda no incluyen objetos ni propiedades a los que el autor de la llamada no tiene acceso.

 

 




