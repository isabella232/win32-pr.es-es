---
title: vararg (atributo)
description: El atributo \ vararg \ especifica que la función toma un número variable de parámetros. Para ello, el último parámetro debe ser una matriz segura de tipo VARIANT que contenga todos los parámetros restantes.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- atributo vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651364"
---
# <a name="vararg-attribute"></a>vararg (atributo)

El atributo **\[ vararg \]** especifica que la función toma un número variable de parámetros. Para ello, el último parámetro debe ser una matriz segura de tipo **Variant** que contenga todos los parámetros restantes.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcional: atributos* 
</dt> <dd>

Especifica cero o más atributos que se van a aplicar a la función. Separe varios atributos con comas.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

El tipo de los datos devueltos por el procedimiento remoto al finalizar.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre del procedimiento remoto.

</dd> <dt>

*Optional-param-Attributes* 
</dt> <dd>

Especifica cero o más atributos que se van a aplicar al parámetro de función inmediatamente después de la lista de atributos.

</dd> <dt>

*lista de parámetros* 
</dt> <dd>

Especifica todos los parámetros, guarda el parámetro final, varying.

</dd> <dt>

*nombre del último parámetro* 
</dt> <dd>

Nombre del parámetro varying.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se pueden aplicar los **\[** [](optional.md) **\]** atributos opcionales o **\[** [**DefaultValue**](defaultvalue.md) **\]** a los parámetros de una función que tenga el atributo **\[ vararg \]** .

## <a name="examples"></a>Ejemplos

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**opta**](optional.md)
</dt> </dl>

 

 