---
title: defaultvalue (atributo)
description: El atributo \defaultvalue\ permite especificar un valor predeterminado para un parámetro opcional con tipo.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- MIDL del atributo defaultvalue
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159627"
---
# <a name="defaultvalue-attribute"></a>defaultvalue (atributo)

El **\[ atributo \] defaultvalue** permite especificar un valor predeterminado para un parámetro opcional con tipo.

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

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*return-type* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función a la que se aplicará el atributo **\[ defaultvalue. \]**

</dd> <dt>

*mandatory-param-list* 
</dt> <dd>

Especifica en o más parámetros necesarios.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos, separados por comas, que se aplican al parámetro .

</dd> <dt>

*param-type* 
</dt> <dd>

Indica el tipo del parámetro opcional.

</dd> <dt>

*param-name* 
</dt> <dd>

Especifica el nombre del parámetro opcional.

</dd> <dt>

*optional-param-list* 
</dt> <dd>

Especifica cero o más parámetros adicionales, cada uno de los cuales debe tener un valor predeterminado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor predeterminado que especifique para el parámetro puede ser cualquier constante, o una expresión que se resuelve como una constante, que se puede representar mediante **variant**. En concreto, no se puede aplicar el atributo **\[ defaultvalue \]** a un parámetro que sea una estructura, una matriz o un **tipo SAFEARRAY.**

El compilador MIDL acepta la siguiente ordenación de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen el **\[ valor \] predeterminado** u atributos **\[** [**opcionales),**](optional.md) **\]**
2.  Parámetros opcionales con o sin el **\[ atributo defaultvalue, \]**
3.  parámetros con el **\[ atributo opcional \]** y sin el atributo **\[ defaultvalue, \]**
4.  **\[**[**parámetro lcid,**](lcid.md) **\]** si lo hay,
5.  **\[**[**retval**](retval.md) **\]** Parámetro

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

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**Opcional**](optional.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 