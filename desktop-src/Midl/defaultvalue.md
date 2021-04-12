---
title: defaultvalue (atributo)
description: El atributo \ DefaultValue \ le permite especificar un valor predeterminado para un parámetro opcional con tipo.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- DefaultValue (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358922"
---
# <a name="defaultvalue-attribute"></a>defaultvalue (atributo)

El atributo **\[ DefaultValue \]** permite especificar un valor predeterminado para un parámetro opcional con tipo.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ DefaultValue \]** .

</dd> <dt>

*lista de parámetros obligatorios* 
</dt> <dd>

Especifica en o más parámetros necesarios.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al parámetro.

</dd> <dt>

*tipo de parámetro* 
</dt> <dd>

Indica el tipo del parámetro opcional.

</dd> <dt>

*param: nombre* 
</dt> <dd>

Especifica el nombre del parámetro opcional.

</dd> <dt>

*opcional-param-List* 
</dt> <dd>

Especifica cero o más parámetros adicionales, cada uno de los cuales debe tener un valor predeterminado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor predeterminado que se especifica para el parámetro puede ser cualquier constante, o una expresión que se resuelve como una constante, que se puede representar mediante una **variante**. En concreto, no se puede aplicar el atributo **\[ \] DefaultValue** a un parámetro que sea una estructura, una matriz o un tipo **SAFEARRAY** .

El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen los atributos **\[ DefaultValue \]** u **\[** [**opcional**](optional.md) **\]** ),
2.  parámetros opcionales con o sin el atributo **\[ DefaultValue \]** ,
3.  parámetros con el atributo **\[ opcional \]** y sin el atributo **\[ DefaultValue \]** ,
4.  **\[** parámetro [**LCID**](lcid.md) **\]** , si existe,
5.  **\[**[**retval**](retval.md) **\]** parámetro

## <a name="examples"></a>Ejemplos

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**opta**](optional.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 