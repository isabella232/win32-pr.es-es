---
title: El encabezado de la interfaz IDL
description: El encabezado de la interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149594"
---
# <a name="the-idl-interface-header"></a>El encabezado de la interfaz IDL

El encabezado de la interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.

Los atributos del encabezado de la interfaz son globales para toda la interfaz. Es decir, se aplican a la interfaz y a todas sus partes. Estos atributos se incluyen entre corchetes al principio de la definición de interfaz. Un ejemplo se muestra en la siguiente definición de interfaz:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Observe que el encabezado de la interfaz contiene los **\[** atributos [**UUID**](/windows/desktop/Midl/uuid) **\]** y **\[** [**version**](/windows/desktop/Midl/version) **\]** . Puesto que representan el UUID y el número de versión de la interfaz, respectivamente, son atributos de toda la interfaz.

El cuerpo de la interfaz también puede contener atributos. Sin embargo, no se aplican a toda la interfaz. Hacen referencia a elementos específicos de la interfaz, como los parámetros de procedimiento remoto.

Para obtener una descripción completa de los atributos del encabezado IDL, vea la [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

 

 