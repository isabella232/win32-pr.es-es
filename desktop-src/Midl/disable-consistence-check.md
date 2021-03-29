---
title: disable_consistency_check atributo)
description: Indica a RPC que no aplique la comprobación de coherencia de la correlación.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356865"
---
# <a name="disable_consistency_check-attribute"></a>deshabilitar \_ atributo de comprobación de coherencia \_

Indica a RPC que no aplique la comprobación de coherencia de la correlación.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

En el caso de los parámetros correlacionados, RPC exigirá que se pase un búfer que no sea NULL cuando la variable Count de correlación no sea NULL.

## <a name="example"></a>Ejemplo

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Si el valor de la *cadena* es **null**, RPC rechazará la llamada a menos que la longitud esté establecida en 0. Tenga en cuenta que RPC permitirá que la *longitud* sea 0, mientras que el valor de la *cadena* no es null, y RPC tratará la *cadena* como una asignación de búfer de longitud 0.

## <a name="remarks"></a>Observaciones

Para deshabilitar esta comprobación, el IDL puede contener \[ el \_ atributo deshabilitar \_ comprobación de coherencia \] en un parámetro, typedef o tipo de puntero. Esto indicará a RPC que no aplique la coherencia entre el puntero de búfer y la variable de correlación del búfer al que apunta el parámetro o el puntero.

Para deshabilitar la comprobación de coherencia para una compilación de MIDL completa (y deshabilitar la aplicación de la comprobación en todos los casos), se puede usar el modificador de la línea de comandos de MIDL [/backward \_ compatible maybenull \_ size](-backward-compat.md) . Esto requiere que el destino de la compilación de MIDL sea al menos â € "Target NT60.

 

 




