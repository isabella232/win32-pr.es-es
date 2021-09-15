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
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473699"
---
# <a name="filteraddobject-function"></a>Función FilterAddObject

La **función FilterAddObject** agrega un único objeto a un [*filtro para mostrar.*](d.md)

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

Controle el filtro de presentación.

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
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE \_ MEMORIA**</dt> </dl>    | Monitor de red no tiene suficiente memoria para crear el objeto.<br/> |



 

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función FilterAddObject.**

Se **llama a la función FilterAddObject** cada vez que se agrega un objeto de filtro al filtro para mostrar. El filtro de presentación es una pila de postfijo de objetos que pueden ser un operador, un valor o una propiedad.

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

 

 




