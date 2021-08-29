---
title: disable_consistency_check atributo
description: Dirige a RPC para que no aplique la comprobación de coherencia de correlación.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc88112ac80462daa6c1babdd29799ccf05e33bb4edb52de1ffbbbb00e71352b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807230"
---
# <a name="disable_consistency_check-attribute"></a>atributo disable \_ consistency \_ check

Dirige a RPC para que no aplique la comprobación de coherencia de correlación.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

En el caso de los parámetros correlacionados, RPC exigirá que se pase un búfer que no sea NULL cuando la variable de recuento de correlación no sea NULL.

## <a name="example"></a>Ejemplo

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Si *MyString* es **NULL,** RPC rechazará la llamada a menos que Length esté establecido en 0. Tenga en cuenta que RPC permitirá *que Length* sea 0 mientras *MyString* no sea NULL y RPC tratará *MyString* como una asignación de búfer de 0 longitud.

## <a name="remarks"></a>Comentarios

Para deshabilitar esta comprobación, el IDL puede contener el atributo disable consistency check en un \[ \_ \_ \] parámetro, typedef o tipo de puntero. Esto hará que RPC no exija la coherencia entre el puntero de búfer y la variable de correlación para el búfer al que apunta el parámetro o puntero.

Para deshabilitar la comprobación de coherencia de una compilación MIDL completa (y deshabilitar la aplicación de la comprobación en todos los casos), se puede usar el modificador de línea de comandos [midL /backward \_ compat maybenull \_ sizeis.](-backward-compat.md) Esto requiere que el destino de la compilación MIDL sea al menos â€"target NT60.

 

 




