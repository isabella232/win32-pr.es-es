---
title: usesgetlasterror (atributo)
description: El atributo \ usesgetlasterror \ indica al llamador que puede llamar a GetLastError para recuperar el código de error.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror (atributo) MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790005"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror (atributo)

El atributo **\[ \] usesgetlasterror** señala al llamador que puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.

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

*module: atributos* 
</dt> <dd>

Cero o más atributos de MIDL que se aplicarán al [**módulo**](module.md).

</dd> <dt>

*nombre del módulo* 
</dt> <dd>

Nombre del identificador del [**módulo**](module.md).

</dd> <dt>

*identificador de entrada* 
</dt> <dd>

Especifica el punto de entrada del módulo, el nombre de la función o el número de identificación de entero.

</dd> <dt>

*otros: atributos* 
</dt> <dd>

Cero o más atributos de MIDL que se aplicarán al procedimiento remoto.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

El tipo de datos que el procedimiento remoto devolverá tras su finalización.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre del procedimiento remoto tal y como se define en el archivo IDL.

</dd> <dt>

*lista de parámetros* 
</dt> <dd>

Cero o más parámetros para el procedimiento remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ \] usesgetlasterror** se puede establecer en un punto de entrada del módulo, si ese punto de entrada utiliza la función de Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver los códigos de error. El atributo indica al llamador que, si se produce un error al llamar a esa función, el autor de la llamada puede llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 