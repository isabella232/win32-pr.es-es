---
title: parámetro/Robust
description: El modificador/Robust indica al compilador de MIDL que genere información adicional de comprobación de errores, que el motor de NDR utiliza para realizar comprobaciones de integridad en tiempo de ejecución.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- parámetro de modificador de/ROBUST MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904021"
---
# <a name="robust-switch"></a>parámetro/Robust

El modificador **/Robust** indica al compilador de MIDL que genere información adicional de comprobación de errores, que el motor de NDR utiliza para realizar comprobaciones de integridad en tiempo de ejecución.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/OIF* 
</dt> <dd>

Estos modificadores son idénticos en su funcionalidad. Especifican el método proxy con código de serialización y usan cadenas de formato rápido para mejorar el rendimiento. Vea/ [**OI**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso del modificador **/Robust** genera información adicional que permite que el motor de representación de datos de red (NDR) realice la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y en punteros de interfaz [**out**](out-idl.md) en aplicaciones DCOM. El modificador **/Robust** solo está disponible en Windows 2000 y versiones posteriores de Windows.

Un argumento correlacionado es un argumento que utiliza cualquiera de los atributos que permiten determinar el tamaño de un objeto de datos en tiempo de ejecución: [**el tamaño \_ es**](size-is.md), la [**longitud \_ es**](length-is.md), el [**primero \_ es**](first-is.md), el [**último \_ es**](last-is.md), el de [**conmutador \_ es**](switch-is.md)y el [**IID \_ es**](iid-is.md). [**\_**](max-is.md) De acuerdo con la especificación de OSF-DCE para la representación de la conexión, este argumento correlacionado aparece en dos lugares diferentes. Por ejemplo, considere un uso típico del **tamaño \_ es** Attribute:

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

En este ejemplo, el cliente pasa un Long que especifica el tamaño de un bloque de tipos de barra \_ (en términos de número de \_ elementos de tipo barra) y un puntero al bloque real de tipos de barra \_ . El argumento de tamaño se correlaciona con el argumento pBarType. De acuerdo con la especificación de OSF-DCE, el argumento de tamaño se representa dos veces en la conexión, primero como en sí mismo y después con la matriz de elementos de tipo de barra \_ que representa el argumento pBarType. No se calculan las referencias de cada argumento de forma independiente, según su propia representación de conexión. Normalmente, el argumento de tamaño y su copia, que se usa para representar parte del otro argumento, tienen los mismos valores. Sin embargo, si el argumento de tamaño está dañado (por ejemplo, cuando el bloque de \_ tipos de barra es mayor que el asignado), la aplicación de servidor puede dejar de responder, ya que usa el valor del argumento size para medir los datos entrantes.

El modificador **/Robust** es necesario para implementar una comprobación de intervalo válida con el atributo de [**intervalo**](range.md) .

## <a name="examples"></a>Ejemplos

**MIDL/Robust/Oicf nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**range**](range.md)
</dt> </dl>

 

 




