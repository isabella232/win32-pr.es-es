---
description: La función FilterAddObject agrega un único objeto a un filtro de visualización.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Función FilterAddObject (Netmon.h)
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
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938738"
---
# <a name="filteraddobject-function"></a>Función FilterAddObject

La **función FilterAddObject** agrega un único objeto a un [*filtro de visualización.*](d.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFilter* \[ En\]
</dt> <dd>

Controle el filtro de visualización.

</dd> <dt>

*lpFilterObject* \[ out\]
</dt> <dd>

Puntero a una [estructura FILTEROBJECT](filterobject.md) que define el objeto que se va a agregar al filtro. Cada objeto puede ser un operador, valor o propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | El *parámetro hFilter* tiene un valor no válido.<br/>                     |
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl>    | Monitor de red no tiene suficiente memoria para crear el objeto.<br/> |



 

## <a name="remarks"></a>Comentarios

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función FilterAddObject.**

Se **llama a la función FilterAddObject** cada vez que se agrega un objeto de filtro al filtro de presentación. El filtro de presentación es una pila de postfijo de objetos que pueden ser un operador, un valor o una propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




