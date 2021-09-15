---
title: Encabezado de interfaz IDL
description: El encabezado de interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476576"
---
# <a name="the-idl-interface-header"></a>Encabezado de interfaz IDL

El encabezado de interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.

Los atributos del encabezado de interfaz son globales para toda la interfaz. Es decir, se aplican a la interfaz y a todas sus partes. Estos atributos se incluyen entre corchetes al principio de la definición de interfaz. En la siguiente definición de interfaz se muestra un ejemplo:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Observe que el encabezado de interfaz contiene los **\[** [**atributos uuid**](/windows/desktop/Midl/uuid) **\]** y **\[** [**version.**](/windows/desktop/Midl/version) **\]** Puesto que representan el UUID y el número de versión de la interfaz respectivamente, son atributos de toda la interfaz.

El cuerpo de la interfaz también puede contener atributos. Sin embargo, no son aplicables a toda la interfaz. Hacen referencia a elementos específicos de la interfaz, como los parámetros de procedimiento remoto.

Para obtener una explicación completa de los atributos de encabezado IDL, consulte la referencia [del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

 

 