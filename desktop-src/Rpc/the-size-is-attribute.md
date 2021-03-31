---
title: El atributo size_is
description: El atributo \ size \_ es \ se asocia a una constante, expresión o variable de tipo entero que especifica el tamaño de asignación de la matriz.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904658"
---
# <a name="the-size_is-attribute"></a>El \[ tamaño \_ es \] Attribute

El \[ [atributo \_ size](/windows/desktop/Midl/size-is) está \] asociado a una constante, expresión o variable de tipo entero que especifica el tamaño de asignación de la matriz. Considere una matriz de caracteres cuya longitud esté determinada por la entrada del usuario:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> El asterisco ( \* ) que marca el marcador de posición para la dimensión de la matriz de variables es opcional.

 

El código auxiliar del servidor debe asignar memoria en el servidor que corresponda a la memoria en el cliente para ese parámetro. La variable que especifica el tamaño siempre debe ser al menos un \[ parámetro [in](/windows/desktop/Midl/in) \] . El atributo direccional **\[ in \]** es necesario para que el valor de tamaño se defina en la entrada al código auxiliar del servidor. Este valor de tamaño proporciona información que el código auxiliar del servidor requiere para asignar la memoria.

El parámetro de tamaño también puede ser \[ in, [out](/windows/desktop/Midl/out-idl) \] . Esto es útil si, por ejemplo, la matriz que envía el cliente no es lo suficientemente grande para los datos que el servidor necesita almacenar en él. Puede usar un parámetro **\[ in, out \]** size para devolver el tamaño requerido al programa cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Varios niveles de punteros](multiple-levels-of-pointers.md)
</dt> </dl>

 

 