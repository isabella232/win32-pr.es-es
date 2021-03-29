---
title: control (atributo)
description: El atributo \ control \ identifica una coclase o biblioteca como control COM, de la que un sitio de contenedor derivará bibliotecas de tipos o clases de objetos de componente adicionales.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- MIDL (atributo de control)
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789867"
---
# <a name="control-attribute"></a>control (atributo)

El atributo **\[ control \]** identifica una [**coclase**](coclass.md) o [**biblioteca**](library.md) como un control com, desde el que un sitio contenedor derivará bibliotecas de tipos o clases de objetos de componente adicionales.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la instrucción [**Library**](library.md) o [**CoClass**](coclass.md) . Separe varios atributos con comas.

</dd> <dt>

*lib o coclassname* 
</dt> <dd>

Especifica el nombre de la [**biblioteca**](library.md) o [**coclase**](coclass.md).

</dd> <dt>

*Figura* 
</dt> <dd>

Instrucciones de MIDL que especifican los miembros de la [**biblioteca**](library.md) o [**coclase**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo le permite marcar las bibliotecas de tipos que describen los controles para que no se muestren en exploradores de tipos destinados a objetos no visuales.

### <a name="flags"></a>Marcas

TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> </dl>

 

 