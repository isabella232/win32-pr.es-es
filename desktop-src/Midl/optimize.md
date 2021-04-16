---
title: Optimize (atributo)
description: El atributo \ Optimize \ ACF se usa para ajustar el nivel de degradado para calcular las referencias de los datos.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- optimizar el atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651326"
---
# <a name="optimize-attribute"></a>Optimize (atributo)

El atributo **\[ apoptimize \]** ACF se usa para ajustar el nivel de degradado para calcular las referencias de los datos.

> [!Note]  
> Esta palabra clave es superceeded y no debe usarse. En su lugar, las compilaciones de MIDL actuales deben usar [**/Oicf**](-oi.md)[**/Robust**](-robust.md) .

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optimización: opciones* 
</dt> <dd>

Especifica el método de cálculo de referencias de datos. Use "s" para la serialización en modo mixto o "i" para el cálculo de referencias interpretado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta versión de RPC proporciona dos métodos para calcular las referencias de datos: modo mixto ("s") e interpretado ("i"). Estos métodos corresponden a los modificadores de la línea de comandos [**/os**](-os.md) y [**/OI**](-oi.md) . El método interpretado calcula las referencias de los datos completamente sin conexión. Aunque esto puede reducir considerablemente el tamaño del código auxiliar, el rendimiento puede verse afectado.

Si el rendimiento es un problema, el método de modo mixto puede ser el mejor enfoque. El modo mixto permite que el compilador de MIDL realice la determinación entre los datos que se van a serializar insertados y los que se calcularán mediante una llamada a una biblioteca de vínculos dinámicos sin conexión. Si muchos procedimientos utilizan los mismos tipos de datos, se puede llamar a un único procedimiento repetidamente para calcular las referencias de los datos. De esta manera, los datos que son más adecuados para el cálculo de referencias en línea se procesan en línea mientras que otros datos se pueden serializar de forma más eficaz sin conexión.

Tenga en cuenta que el atributo **\[ Optimize \]** se puede usar como atributo de interfaz o como atributo de operación. Si se usa como atributo de interfaz, establece el valor predeterminado para toda la interfaz, invalidando los modificadores de la línea de comandos. Sin embargo, si se usa como atributo de operación, solo afecta a esa operación, invalidando los modificadores de la línea de comandos y el valor predeterminado de la interfaz.

## <a name="examples"></a>Ejemplos

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




