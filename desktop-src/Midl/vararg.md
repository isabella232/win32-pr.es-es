---
title: vararg (atributo)
description: El atributo \rg\ especifica que la función toma un número variable de parámetros. Para ello, el último parámetro debe ser una matriz segura de tipo VARIANT que contenga todos los parámetros restantes.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- atributo midl de segorg
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848393f6bad82d6793e34ba6f4da803c7dd64803c1c40e4ea05487ea141ec48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641013"
---
# <a name="vararg-attribute"></a>vararg (atributo)

El **\[ atributo \] perorg** especifica que la función toma un número variable de parámetros. Para ello, el último parámetro debe ser una matriz segura de tipo **VARIANT** que contenga todos los parámetros restantes.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optional-attributes* 
</dt> <dd>

Especifica cero o más atributos que se aplicarán a la función. Separe varios atributos con comas.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo de los datos devueltos por el procedimiento remoto tras la finalización.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre del procedimiento remoto.

</dd> <dt>

*optional-param-attributes* 
</dt> <dd>

Especifica cero o más atributos que se aplicarán al parámetro de función inmediatamente después de la lista de atributos.

</dd> <dt>

*param-list* 
</dt> <dd>

Especifica todos los parámetros y guarda el parámetro final, variable.

</dd> <dt>

*last-param-name* 
</dt> <dd>

Nombre del parámetro variable.

</dd> </dl>

## <a name="remarks"></a>Comentarios

No se pueden aplicar los **\[** [**atributos**](optional.md) **\]** **\[** [**opcionales o defaultvalue**](defaultvalue.md) **\]** a ningún parámetro de una función que tenga el atributo **\[ segorg. \]**

## <a name="examples"></a>Ejemplos

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Opcional**](optional.md)
</dt> </dl>

 

 