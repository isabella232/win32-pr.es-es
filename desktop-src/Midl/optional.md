---
title: optional (atributo)
description: El atributo \ optional\ especifica un parámetro opcional para una función miembro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- atributo opcional MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159431"
---
# <a name="optional-attribute"></a>optional (atributo)

El **\[ atributo \]** opcional especifica un parámetro opcional para una función miembro.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*return-type* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función tal como se define en el archivo IDL.

</dd> <dt>

*otros atributos* 
</dt> <dd>

Cero o más atributos MIDL opcionales.

</dd> <dt>

*parameter-type* 
</dt> <dd>

Tipo de datos del parámetro opcional.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el nombre del parámetro opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \]** opcional solo es válido si el parámetro es de tipo **VARIANT** o **VARIANT** Â \* .

El compilador MIDL acepta la siguiente ordenación de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen el **\[** [**valor predeterminado**](defaultvalue.md) **\]** u atributos **\[ opcionales), \]**
2.  Parámetros opcionales con o sin el **\[** [**atributo defaultvalue,**](defaultvalue.md) **\]**
3.  Parámetros con el **\[ atributo opcional \]** y sin el atributo **\[** [**defaultvalue,**](defaultvalue.md) **\]**
4.  **\[**[**Parámetro lcid,**](lcid.md) **\]** si hay alguno,
5.  **\[**[**retval**](retval.md) **\]** Parámetro

No se puede aplicar **\[ el \] atributo** opcional a un parámetro que también tenga los atributos **\[** [**lcid**](lcid.md) o **\]** **\[** [**retval.**](retval.md) **\]**

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Retval**](retval.md)
</dt> </dl>

 

 