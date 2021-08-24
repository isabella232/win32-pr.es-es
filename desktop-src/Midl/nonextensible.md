---
title: nonextensible (atributo)
description: El atributo \nonextensible\ especifica que la implementación de IDispatch solo incluye las propiedades y los métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- atributo nonextensible MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c4e55cf5cf2c05ff9c3619b19e7a9b0582f3cf64bc0f9a711fb1af274bfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066885"
---
# <a name="nonextensible-attribute"></a>nonextensible (atributo)

El **\[ atributo nonextensible \]** especifica que la implementación de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) solo incluye las propiedades y métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución. (De forma predeterminada, Automation supone que las interfaces pueden agregar miembros en tiempo de ejecución; es decir, se supone que son extensibles).

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la [**interfaz**](interface.md).

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos de interfaz MIDL.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instrucciones IDL que forman la definición de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede aplicar el **\[ atributo nonextensible \]** a una interfaz o a una interfaz dispinterface. Sin embargo, una interfaz también debe tener **\[** [**los atributos dual**](dual.md) y **\]** **\[** [**oleautomation.**](oleautomation.md) **\]**

### <a name="flags"></a>Marcas

TYPEFLAG \_ FNONEXTENSIBLE

## <a name="examples"></a>Ejemplos

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Contenido de una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[**Doble**](dual.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 