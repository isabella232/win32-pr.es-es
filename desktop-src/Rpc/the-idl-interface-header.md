---
title: Encabezado de interfaz IDL
description: El encabezado de interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c176078c370819331405b070ffa832384584a944b65fae771b9a2044a178e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924274"
---
# <a name="the-idl-interface-header"></a>Encabezado de interfaz IDL

El encabezado de interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.

Los atributos del encabezado de interfaz son globales para toda la interfaz. Es decir, se aplican a la interfaz y a todas sus partes. Estos atributos se incluyen entre corchetes al principio de la definición de la interfaz. En la siguiente definición de interfaz se muestra un ejemplo:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Observe que el encabezado de interfaz contiene los **\[** [**atributos uuid**](/windows/desktop/Midl/uuid) **\]** y **\[** [**version.**](/windows/desktop/Midl/version) **\]** Dado que representan el UUID y el número de versión de la interfaz respectivamente, son atributos de toda la interfaz.

El cuerpo de la interfaz también puede contener atributos. Sin embargo, no son aplicables a toda la interfaz. Hacen referencia a elementos específicos de la interfaz, como los parámetros de procedimiento remoto.

Para obtener una explicación completa de los atributos de encabezado IDL, consulte la referencia [del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

 

 