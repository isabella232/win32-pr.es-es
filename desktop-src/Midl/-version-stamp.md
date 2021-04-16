---
title: modificador/version_stamp
description: El \_ modificador de marca/version suprime la generación de macros que especifican el número de versión mínimo necesario del archivo de encabezado RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp modificador MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685637"
---
# <a name="version_stamp-switch"></a>\_cambio de marca/version

El modificador de **\_ marca/version** suprime la generación de macros que especifican el número de versión mínimo necesario del archivo de encabezado RPC, Rpcndr. h.

Las nuevas características de MIDL pueden requerir definiciones adicionales para compilar el código auxiliar correctamente, por lo que el código auxiliar tiene macros que comprueban la compatibilidad entre los archivos binarios MIDL y el entorno de compilación. Es posible que tenga que usar este modificador si mueve MIDL a un entorno de compilación diferente del que instaló por primera vez los archivos binarios de MIDL.

Tenga en cuenta que no se admite la combinación de entornos de compilación.

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

 

 




