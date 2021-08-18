---
title: atributo de control
description: El atributo \ control\ identifica una coclase o biblioteca como un control COM, del que un sitio de contenedor derivará bibliotecas de tipos adicionales o clases de objeto de componente.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- atributo de control MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6372ffb7f7d9f19769e419b12c0b109736a9867360224e023f1b622c653854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643684"
---
# <a name="control-attribute"></a>atributo de control

El atributo de **\[ control \]** identifica [](library.md) una [**coclase**](coclass.md) o biblioteca como un control COM, del que un sitio de contenedor derivará bibliotecas de tipos adicionales o clases de objetos de componente.

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

*attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la [**biblioteca o**](library.md) a la instrucción de [**la coclase.**](coclass.md) Separe varios atributos con comas.

</dd> <dt>

*lib-or-coclassname* 
</dt> <dd>

Especifica el nombre de la biblioteca [**o**](library.md) [**de la coclase**](coclass.md).

</dd> <dt>

*Definiciones* 
</dt> <dd>

Instrucciones MIDL que especifican los miembros de la [**biblioteca o**](library.md) [**la coclase**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este atributo permite marcar bibliotecas de tipos que describen controles para que no se muestren en exploradores de tipos destinados a objetos novisuales.

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

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> </dl>

 

 