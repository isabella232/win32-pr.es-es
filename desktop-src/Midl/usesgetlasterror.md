---
title: usesgetlasterror (atributo)
description: El atributo \ usesgetlasterror\ indica al autor de la llamada que puede llamar a GetLastError para recuperar el código de error.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- atributo usesgetlasterror MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239486792eb218d51c305f9955331e90c6c165586153dab167f2e19d3a0324e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641040"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror (atributo)

El **\[ atributo usesgetlasterror \]** indica al autor de la llamada que puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*module-attributes* 
</dt> <dd>

Cero o más atributos MIDL que se aplicarán al [**módulo**](module.md).

</dd> <dt>

*module-name* 
</dt> <dd>

Nombre del identificador del [**módulo**](module.md).

</dd> <dt>

*entry-id* 
</dt> <dd>

Especifica el punto de entrada del módulo: nombre de función o número de identificación de enteros.

</dd> <dt>

*otros atributos* 
</dt> <dd>

Cero o más atributos MIDL que se aplicarán al procedimiento remoto.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo de los datos que devolverá el procedimiento remoto tras la finalización.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre del procedimiento remoto tal como se define en el archivo IDL.

</dd> <dt>

*param-list* 
</dt> <dd>

Cero o más parámetros para el procedimiento remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \] usesgetlasterror** se puede establecer en un punto de entrada de módulo, si ese punto de entrada usa la función [**Windows SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver códigos de error. El atributo indica al autor de la llamada que, si se produce un error al llamar a esa función, el autor de la llamada puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.

## <a name="examples"></a>Ejemplos

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 