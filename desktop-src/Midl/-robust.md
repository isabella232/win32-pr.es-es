---
title: Modificador /robust
description: El modificador /robust indica al compilador MIDL que genere información adicional de comprobación de errores, que el motor MUTACIÓN usa para realizar comprobaciones de integridad en tiempo de ejecución.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robust switch MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551f5a60013aa3a903dcb3e35cc4c25a9f83dc67fff2a6ab5c7bfd62a041feee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895835"
---
# <a name="robust-switch"></a>Modificador /robust

El **modificador /robust** indica al compilador MIDL que genere información adicional de comprobación de errores, que el motor MUTACIÓN usa para realizar comprobaciones de integridad en tiempo de ejecución.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/Oif* 
</dt> <dd>

Estos modificadores son idénticos en su funcionalidad. Especifican el método de proxy sin código de serialización y usan cadenas de formato rápido para mejorar el rendimiento. Vea / [**Oi**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

El uso del modificador **/robust** genera información adicional que permite que el motor de representación de datos de red ( [](out-idl.md) RAID) realice la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y punteros de interfaz de salida en aplicaciones DCOM. El **modificador /robust** solo está disponible en Windows 2000 y versiones posteriores de Windows.

Un argumento correlacionado es un argumento que usa cualquiera de los atributos que permiten determinar el tamaño de un objeto de datos en tiempo de ejecución: [**size \_ es**](size-is.md), length es , first es [**, \_**](first-is.md) [**\_ last**](last-is.md)es , max es , [**switch \_ es**](switch-is.md)y [**iid \_ es**](iid-is.md). [**\_**](length-is.md) [**\_**](max-is.md) De acuerdo con la especificación de OSF-DCE para la representación de conexión, este argumento correlacionado aparece en dos lugares diferentes. Por ejemplo, considere un uso típico del **atributo size \_ is:**

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

En este ejemplo, el cliente pasa un valor long que especifica el tamaño de un bloque de ERRORES TIPOGRÁFICOS DE BARRA (en términos de número de elementos BAR TYPES) y un puntero al bloque real de ERRORES TIPOGRÁFICOS \_ \_ \_ BAR. El argumento Size se correlaciona con el argumento pBarType. De acuerdo con la especificación de OSF-DCE, el argumento Size se representa dos veces en la conexión, primero como a sí mismo y luego con la matriz de elementos BAR TYPE que representan el \_ argumento pBarType. Cada argumento se desmarsa de forma independiente, según su propia representación de conexión. Normalmente, el argumento Size y su copia, que se usan para representar parte del otro argumento, tienen los mismos valores. Sin embargo, si el argumento Size se daña (por ejemplo, cuando el bloque de BAR TYPES es mayor que el asignado), la aplicación de servidor puede dejar de responder, ya que usa el valor del argumento Size para medir los datos \_ entrantes.

El **modificador /robust** es necesario para implementar la comprobación de intervalos válida con el [**atributo range.**](range.md)

## <a name="examples"></a>Ejemplos

**midl /robust /Oicf filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**range**](range.md)
</dt> </dl>

 

 




