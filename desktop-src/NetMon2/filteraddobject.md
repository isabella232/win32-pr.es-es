---
description: La función FilterAddObject agrega un solo objeto a un filtro de presentación.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Función FilterAddObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497002"
---
# <a name="filteraddobject-function"></a>FilterAddObject función)

La función **FilterAddObject** agrega un solo objeto a un [*filtro de presentación*](d.md).

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFilter* \[ de\]
</dt> <dd>

Identificador del filtro de presentación.

</dd> <dt>

*lpFilterObject* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [FILTEROBJECT](filterobject.md) que define el objeto que se va a agregar al filtro. Cada objeto puede ser un operador, un valor o una propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ parámetro no válido \_**</dt> </dl> | El parámetro *hFilter* tiene un valor no válido.<br/>                     |
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl>    | Monitor de red no tiene suficiente memoria para crear el objeto.<br/> |



 

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **FilterAddObject** .

Se llama a la función **FilterAddObject** cada vez que se agrega un objeto de filtro al filtro de presentación. El filtro de visualización es una pila de objetos postfijo que puede ser un operador, un valor o una propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




