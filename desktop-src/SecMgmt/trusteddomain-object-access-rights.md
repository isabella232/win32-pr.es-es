---
description: Enumera y explica los derechos de acceso del objeto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Derechos de acceso a objetos TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efeaf621cc3727cb936e69806bbcf89dabe5d41eb39b38dce3f9f23a0200dcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893013"
---
# <a name="trusteddomain-object-access-rights"></a>Derechos de acceso a objetos TrustedDomain

El [**tipo de objeto TrustedDomain**](trusteddomain-object.md) tiene los siguientes tipos de acceso:



| Tipo de acceso                  | Descripción                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| NOMBRE DE \_ DOMINIO DE CONSULTA DE \_ \_ CONFIANZA | Este tipo de acceso es necesario para consultar el nombre del dominio de confianza.              |
| CONTROLADORES DE \_ CONJUNTO \_ DE CONFIANZA    | Este tipo de acceso es necesario para establecer la lista de controladores del dominio de confianza. |
| POSIX \_ DE \_ CONSULTA DE CONFIANZA        | Este tipo de acceso es necesario para recuperar el desplazamiento de id. de Posix de un dominio de confianza.  |
| TRUSTED \_ SET \_ POSIX          | Este tipo de acceso es necesario para establecer el desplazamiento de id. de Posix de un dominio de confianza.       |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genérico

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

Este objeto no admite el tipo de acceso estándar SYNCHRONIZE (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



