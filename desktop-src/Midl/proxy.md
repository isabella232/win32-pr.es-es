---
title: atributo proxy
description: El atributo \proxy\ impide que Automation se registre como controlador de proxy/stub para una interfaz dual.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- atributo de proxy MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159407"
---
# <a name="proxy-attribute"></a>atributo proxy

El **\[ atributo de proxy \]** impide que Automation se registre como controlador de proxy/stub para una interfaz dual.

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

Especifica una cadena que consta de 8 dígitos hexadecimales seguidos de un guion, tres grupos de 4 dígitos hexadecimales cada uno seguidos de un guion y, a continuación, 12 dígitos hexadecimales. Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador del compilador MIDL [**/osf**](-osf.md).

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

## <a name="remarks"></a>Observaciones

El uso del \[ **atributo proxy** \] para una interfaz dual impide que el TLB se haga cargo de los códigos auxiliares generados. Si se especifica este atributo, no se debe anular el registro del proxy de la lista de tipos cuando se anula el registro de la base de datos typelib.

### <a name="flags"></a>Marcas

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY
</dt> <dd>

Las interfaces se pueden marcar con la marca TYPEFLAG PROXY para indicar que usarán una biblioteca de vínculos dinámicos de \_ proxy/stub. Esta marca especifica que el proxy de la lista de tipos no debe anularse del registro cuando se anula el registro de la base de datos typelib.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Generar una biblioteca de tipos con MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Doble**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 