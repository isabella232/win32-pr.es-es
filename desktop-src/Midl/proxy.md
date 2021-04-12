---
title: atributo proxy
description: El atributo \ proxy \ impide que la automatización se registre como un controlador de proxy o código auxiliar para una interfaz dual.
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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487542"
---
# <a name="proxy-attribute"></a>atributo proxy

El atributo **\[ proxy \]** impide que la automatización se registre como un controlador de proxy o código auxiliar para una interfaz dual.

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

*cadena: UUID* 
</dt> <dd>

Especifica una cadena que consta de 8 dígitos hexadecimales seguidos de un guion y, a continuación, tres grupos de 4 dígitos hexadecimales, seguidos de un guion y 12 dígitos hexadecimales. Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).

</dd> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto. Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de la que esta interfaz derivada hereda las funciones miembro, los códigos de estado y los atributos de interfaz. La interfaz derivada no hereda las definiciones de tipo. Para ello, use la palabra clave [**Import**](import.md) para importar el archivo IDL de la interfaz base.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso del \[ atributo **proxy** \] para una interfaz dual impide que el TLB tome el código auxiliar generado. Si se especifica este atributo, no se debe anular el registro del proxy typelib cuando se anula el registro de typelib.

### <a name="flags"></a>Marcas

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG
</dt> <dd>

Las interfaces se pueden marcar con la \_ marca del proxy TYPEFLAG para indicar que van a usar una biblioteca de vínculos dinámicos de proxy/código auxiliar. Esta marca especifica que no se debe anular el registro del proxy de la biblioteca de bibliotecas cuando se anula el registro de la biblioteca de bibliotecas.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Generar una biblioteca de tipos con MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**BI**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 