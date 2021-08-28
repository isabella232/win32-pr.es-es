---
title: atributo proxy
description: El atributo \ proxy\ impide que Automation se registre como controlador de proxy o stub para una interfaz dual.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- ATRIBUTO DE PROXY MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641425"
---
# <a name="proxy-attribute"></a>atributo proxy

El **\[ atributo proxy \]** impide que Automation se registre como controlador de proxy/stub para una interfaz dual.

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string-uuid* 
</dt> <dd>

Especifica una cadena formada por 8 dígitos hexadecimales seguidos de un guión, tres grupos de 4 dígitos hexadecimales cada uno seguidos de un guion y, a continuación, 12 dígitos hexadecimales. Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador del compilador MIDL [**/osf**](-osf.md).

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en su conjunto. Cuando hay dos o más atributos de interfaz, deben estar separados por comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de la que esta interfaz derivada hereda funciones miembro, códigos de estado y atributos de interfaz. La interfaz derivada no hereda definiciones de tipo. Para ello, use la palabra [**clave import**](import.md) para importar el archivo IDL de la interfaz base.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El uso del \[ **atributo de proxy** para una interfaz dual impide que el \] TLB se haga cargo de los códigos auxiliares generados. Si se especifica este atributo, no se debe anular el registro del proxy de la lista de tipos cuando se anula el registro de la lista de tipos.

### <a name="flags"></a>Marcas

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY
</dt> <dd>

Las interfaces se pueden marcar con la marca TYPEFLAG PROXY para indicar que usarán una biblioteca de vínculos dinámicos \_ proxy/stub. Esta marca especifica que no se debe anular el registro del proxy de la lista de tipos cuando se anula el registro de la lista de tipos.

</dd> </dl>

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Generar una biblioteca de tipos con MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Doble**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 