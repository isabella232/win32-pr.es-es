---
title: optional (atributo)
description: El atributo \ Optional \ especifica un parámetro opcional para una función miembro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- parámetro opcional MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904589"
---
# <a name="optional-attribute"></a>optional (atributo)

El atributo **\[ opcional \]** especifica un parámetro opcional para una función miembro.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función tal y como se define en el archivo IDL.

</dd> <dt>

*otros: atributos* 
</dt> <dd>

Cero o más atributos de MIDL opcionales.

</dd> <dt>

*tipo de parámetro* 
</dt> <dd>

El tipo de datos del parámetro opcional.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el nombre del parámetro opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ opcional \]** solo es válido si el parámetro es de tipo **Variant** o **Variant** Â \* .

El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen los **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** u **\[ opcional \]** ),
2.  Parámetros opcionales con o sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,
3.  Parámetros con el atributo **\[ opcional \]** y sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,
4.  **\[** parámetro [**LCID**](lcid.md) **\]** , si existe,
5.  **\[**[**retval**](retval.md) **\]** parámetro

No se puede aplicar el atributo **\[ opcional \]** a un parámetro que también tenga los **\[** atributos [**LCID**](lcid.md) **\]** o **\[** [**retval**](retval.md) **\]** .

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 