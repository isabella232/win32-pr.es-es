---
title: modificador/msc_ver
description: El \_ modificador/MSC ver se usa para permitir que MIDL genere código que incluye optimizaciones para diferentes versiones de los compiladores de C/C++ de Microsoft.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver modificador MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904174"
---
# <a name="msc_ver-switch"></a>\_modificador de/MSC ver

El modificador **/MSC \_ Ver** se usa para permitir que MIDL genere código que incluye optimizaciones para diferentes versiones de los compiladores de C/C++ de Microsoft.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*número de versión \_* 
</dt> <dd>

Especifica un número de versión entero del compilador Microsoft Visual C++ que se utilizará para compilar el cliente y el código auxiliar del servidor de la aplicación distribuida. El número de versión predeterminado es 1100, que corresponde a Visual C++ versión 5,0. El número de versión 1200 corresponde a Visual C++ versión 6,0, etc.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En concreto, los valores de versión de 1100 o superior hacen que el compilador de MIDL genere código mediante la directiva **\_ \_ declspec (UUID ())** . También activa macros que usan las directivas **\_ \_ declspec (selectany)** y **\_ \_ declspec (novtable)** .

 

 




