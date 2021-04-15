---
description: Enumera y explica los derechos de acceso del objeto de datos privado.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Derechos de acceso a objetos de datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497188"
---
# <a name="private-data-object-access-rights"></a>Derechos de acceso a objetos de datos privados

Los tipos de acceso de este tipo de objeto son:



| Tipo de acceso          | Descripción                                      |
|----------------------|--------------------------------------------------|
| \_valor de consulta Secret \_ | Este tipo de acceso es necesario para recuperar un secreto. |
| \_valor del conjunto de secretos \_   | Este tipo de acceso es necesario para modificar un secreto.   |



 

## <a name="generic-access-masks"></a>Máscaras de acceso genéricas

Este tipo de objeto tiene las siguientes asignaciones de acceso genérico:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Tipos de acceso estándar:

Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional). Se admiten todos los tipos de acceso necesarios. La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



