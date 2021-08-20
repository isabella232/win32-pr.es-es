---
title: noncreatable (atributo)
description: El atributo \noncreatable\ define un objeto al que no se pueden crear instancias por sí mismo.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL de atributo nocreable
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e59c53d8e4c05d15d55a6ccd9d7fb2b5cd8783463d1f59d439c74240fdd93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066945"
---
# <a name="noncreatable-attribute"></a>noncreatable (atributo)

El **\[ atributo no \] creable** define un objeto al que no se pueden crear instancias por sí mismo.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la clase .

</dd> <dt>

*coclass-name* 
</dt> <dd>

Nombre de la clase.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Lista de interfaces para la clase .

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use el atributo **\[ \] nocreatable** en una instrucción [**coclass**](coclass.md) para indicar a los usuarios que no pueden crear un nuevo objeto de esta clase en el nivel superior, es decir, mediante una llamada a **CreateInstance** o **CoCreateInstance**. La creación de instancias de un objeto de esta clase requiere una llamada de método a otro objeto. Por ejemplo, en Microsoft Excel, el objeto "Cell" no es decreable y se debe obtener de un objeto Microsoft Excel Worksheet.

Los métodos que devuelven instancias de clases nocreables deben devolver el tipo exacto del objeto, en lugar de **los** tipos VARIANT **o IDispatch.** \*

### <a name="typeflag-representation"></a>Representación de tipoflag:

Ausencia de TYPEFLAG \_ FCANCREATE.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 