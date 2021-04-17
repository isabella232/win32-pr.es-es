---
title: requestedit (atributo)
description: El atributo \ requestedit \ indica que la propiedad admite la notificación OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit (atributo) MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651350"
---
# <a name="requestedit-attribute"></a>requestedit (atributo)

El atributo **\[ \] requestedit** indica que la propiedad admite la notificación **OnRequestEdit** .

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcional: atributos* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La compatibilidad con la notificación de **OnRequestEdit** significa que, antes de que se realice un cambio, el objeto enviará al cliente una solicitud de permiso para cambiar una propiedad. Un objeto puede admitir el enlace de datos pero no tiene este atributo.

### <a name="flags"></a>Marcas

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Ejemplos

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 