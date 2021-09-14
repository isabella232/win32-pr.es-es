---
title: entry (atributo)
description: El atributo \ entry\ especifica una función exportada o una constante en un módulo mediante la identificación del punto de entrada en el archivo DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- atributo de entrada MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159597"
---
# <a name="entry-attribute"></a>entry (atributo)

El **\[ atributo \]** entry especifica una función exportada o una constante en un módulo mediante la identificación del punto de entrada en el archivo DLL.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universalmente para el [**módulo**](module.md).

</dd> <dt>

*entry-id* 
</dt> <dd>

Especifica el nombre de la función de punto de entrada del módulo o el número de identificación de entero.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica cero o más atributos para que el compilador MIDL se aplique al [**módulo**](module.md).

</dd> <dt>

*modulename* 
</dt> <dd>

Especifica el nombre que usan otros componentes de software para indicar el [**módulo**](module.md).

</dd> <dt>

*elementlist* 
</dt> <dd>

Especifica una o varias instrucciones de definición de elemento de módulo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la *variable entryid* del atributo **\[ \] de** entrada es una cadena, se trata de un punto de entrada con nombre. Si *entryid* es un número, el punto de entrada se define mediante un ordinal. Este atributo proporciona una manera de obtener la dirección de una función en un módulo.

## <a name="examples"></a>Ejemplos

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Módulo**](module.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 