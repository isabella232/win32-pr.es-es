---
title: El size_is atributo
description: El atributo \size is\ está asociado a una constante, expresión o variable de entero que especifica el \_ tamaño de asignación de la matriz.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361882"
---
# <a name="the-size_is-attribute"></a>El \[ tamaño \_ es \] Attribute

El atributo size is está asociado a una constante, expresión o variable de entero que especifica el tamaño de \[ [ \_ ](/windows/desktop/Midl/size-is) \] asignación de la matriz. Considere una matriz de caracteres cuya longitud viene determinada por la entrada del usuario:

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
> El asterisco ( \* ) que marca el marcador de posición para la dimensión variable-array es opcional.

 

El código auxiliar del servidor debe asignar memoria en el servidor correspondiente a la memoria del cliente para ese parámetro. La variable que especifica el tamaño siempre debe ser al menos un \[ [parámetro in.](/windows/desktop/Midl/in) \] El **\[ atributo direccional \]** es necesario para que el valor de tamaño se defina en la entrada al código auxiliar del servidor. Este valor de tamaño proporciona información que el código auxiliar del servidor requiere para asignar la memoria.

El parámetro size también puede estar \[ en, [out](/windows/desktop/Midl/out-idl) \] . Esto resulta útil si, por ejemplo, la matriz que envía el cliente no es lo suficientemente grande para los datos que el servidor necesita almacenar en ella. Puede usar un **\[ parámetro \] de tamaño de entrada** y salida para devolver el tamaño necesario al programa cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Varios niveles de punteros](multiple-levels-of-pointers.md)
</dt> </dl>

 

 