---
description: Enumera y explica los derechos de acceso del objeto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Derechos de acceso a objetos de TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686668"
---
# <a name="trusteddomain-object-access-rights"></a>Derechos de acceso a objetos de TrustedDomain

El tipo de objeto [**TrustedDomain**](trusteddomain-object.md) tiene los siguientes tipos de acceso:



| Tipo de acceso                  | Descripción                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| \_nombre de \_ dominio de consulta de confianza \_ | Este tipo de acceso es necesario para consultar el nombre del dominio de confianza.              |
| \_controladores de conjuntos de confianza \_    | Este tipo de acceso es necesario para establecer la lista de controladores del dominio de confianza. |
| \_POSIX de consulta de confianza \_        | Este tipo de acceso es necesario para recuperar el desplazamiento de identificador POSIX de un dominio de confianza.  |
| \_POSIX de conjunto de confianza \_          | Este tipo de acceso es necesario para establecer el desplazamiento de identificador POSIX de un dominio de confianza.       |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genéricas

Este tipo de objeto tiene las siguientes asignaciones de acceso genérico:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Tipos de acceso estándar

Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



