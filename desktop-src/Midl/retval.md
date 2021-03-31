---
title: retval (atributo)
description: El atributo/retval \ designa el parámetro que recibe el valor devuelto del miembro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- atributo de retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904523"
---
# <a name="retval-attribute"></a>retval (atributo)

El atributo **\[ retval \]** designa el parámetro que recibe el valor devuelto del miembro.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de valor devuelto* 
</dt> <dd>

El tipo de datos del valor devuelto del procedimiento remoto.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre que se usa para invocar el procedimiento remoto.

</dd> <dt>

*opcional: atributos* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*tipo de datos* 
</dt> <dd>

Tipo de los datos que se pasan a través del parámetro.

</dd> <dt>

*param: nombre* 
</dt> <dd>

Nombre del identificador del parámetro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar el atributo **\[ retval \]** en los parámetros de los miembros de interfaz que describen métodos u obtienen propiedades. (El atributo es obligatorio en el último parámetro de un método que tenga **\[** [**propget**](propget.md) **\]** atributo). El parámetro debe tener el **\[** atributo [**out**](out-idl.md) **\]** y debe ser un tipo de puntero.

No se puede aplicar el **\[** atributo [**opcional**](optional.md) **\]** a un parámetro **\[ \] retval** .

El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen los **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** u **\[** [**opcional**](optional.md) **\]** ).
2.  Parámetros opcionales con o sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .
3.  Parámetros con el **\[** atributo [**opcional**](optional.md) **\]** y sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .
4.  **\[** parámetro [**LCID**](lcid.md) **\]** , si existe.
5.  parámetro **\[ retval \]** .

Los parámetros con el atributo **\[ retval \]** no se muestran en exploradores orientados al usuario.

### <a name="flags"></a>Marcas

IDLFLAG \_ FRETVAL

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
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

[**opta**](optional.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 