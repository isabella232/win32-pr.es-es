---
title: retval (atributo)
description: El atributo \ retval\ designa el parámetro que recibe el valor devuelto del miembro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- atributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159392"
---
# <a name="retval-attribute"></a>retval (atributo)

El **\[ atributo \] retval** designa el parámetro que recibe el valor devuelto del miembro.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*return-type* 
</dt> <dd>

Tipo de datos del valor devuelto del procedimiento remoto.

</dd> <dt>

*function-name* 
</dt> <dd>

Nombre utilizado para invocar el procedimiento remoto.

</dd> <dt>

*optional-attributes* 
</dt> <dd>

Cero o más atributos MIDL.

</dd> <dt>

*tipo de datos* 
</dt> <dd>

Tipo de los datos pasados a través del parámetro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nombre del identificador del parámetro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar el atributo **\[ retval \] en** parámetros de miembros de interfaz que describen métodos u obtienen propiedades. (El atributo es necesario en el último parámetro de un método que tiene el **\[** [**propget**](propget.md) **\]** attribute).) El parámetro debe tener el **\[** [**atributo out**](out-idl.md) **\]** y debe ser un tipo de puntero.

No se puede aplicar el **\[** [**atributo**](optional.md) **\]** opcional a un parámetro **\[ retval. \]**

El compilador MIDL acepta la siguiente ordenación de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen el **\[** [**valor predeterminado**](defaultvalue.md) **\]** u atributos **\[** [**opcionales).**](optional.md) **\]**
2.  Parámetros opcionales con o sin el **\[** [**atributo defaultvalue.**](defaultvalue.md) **\]**
3.  Parámetros con el **\[** [**atributo opcional**](optional.md) **\]** y sin el atributo **\[** [**defaultvalue.**](defaultvalue.md) **\]**
4.  **\[**[**Parámetro lcid,**](lcid.md) **\]** si lo hay.
5.  **\[ parámetro \] retval.**

Los parámetros con **\[ el atributo retval \]** no se muestran en los exploradores orientados al usuario.

### <a name="flags"></a>Marcas

IDLFLAG \_ ESTAVAL

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
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

[**Opcional**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 