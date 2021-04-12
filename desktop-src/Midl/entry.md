---
title: entry (atributo)
description: El atributo \ entry \ especifica una función exportada o una constante en un módulo mediante la identificación del punto de entrada en el archivo DLL.
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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358843"
---
# <a name="entry-attribute"></a>entry (atributo)

El atributo de **\[ entrada \]** especifica una función o constante exportada en un módulo mediante la identificación del punto de entrada en el archivo dll.

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

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para el [**módulo**](module.md).

</dd> <dt>

*identificador de entrada* 
</dt> <dd>

Especifica el nombre de función del punto de entrada del módulo o el número de identificación de entero.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos para que el compilador de MIDL los aplique al [**módulo**](module.md).

</dd> <dt>

*ModuleName* 
</dt> <dd>

Especifica el nombre que otros componentes de software usan para denotar el [**módulo**](module.md).

</dd> <dt>

*elementlist* 
</dt> <dd>

Especifica una o más instrucciones de definición de elementos de módulo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la variable *EntryID* del atributo de **\[ entrada \]** es una cadena, se trata de un punto de entrada con nombre. Si *EntryID* es un número, el punto de entrada se define mediante un ordinal. Este atributo proporciona una manera de obtener la dirección de una función en un módulo.

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

[**DllName**](dllname-str-.md)
</dt> <dt>

[**destina**](module.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 