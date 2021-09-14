---
title: nonextensible (atributo)
description: El atributo \nonextensible\ especifica que la implementación de IDispatch solo incluye las propiedades y los métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nonextensible attribute MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159444"
---
# <a name="nonextensible-attribute"></a>nonextensible (atributo)

El **\[ atributo nonextensible \]** especifica que la implementación de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) incluye solo las propiedades y los métodos enumerados en la descripción de la interfaz y no se puede extender con miembros adicionales en tiempo de ejecución. (De forma predeterminada, Automation da por supuesto que las interfaces pueden agregar miembros en tiempo de ejecución; es decir, supone que son extensibles).

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

## <a name="remarks"></a>Observaciones

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

 

 