---
title: función glDeleteLists (GL. h)
description: La función glDeleteLists elimina un grupo contiguo de listas de presentación.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists (función) OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676783"
---
# <a name="gldeletelists-function"></a>glDeleteLists función)

La función **glDeleteLists** elimina un grupo contiguo de listas de presentación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*list* 
</dt> <dd>

Nombre entero de la primera lista de visualización que se va a eliminar.

</dd> <dt>

*range* 
</dt> <dd>

Número de listas de presentación que se van a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glDeleteLists** hace que se elimine un grupo contiguo de listas de presentación. El parámetro *List* es el nombre de la primera lista de visualización que se va a eliminar y *Range* es el número de listas de presentación que se van a eliminar. Se eliminan todas las listas de pantallas *d* *con*  =    =    +  el *intervalo* de lista d de lista 1.

Todas las ubicaciones de almacenamiento asignadas a las listas de visualización especificadas se liberan y los nombres están disponibles para su reutilización en un momento posterior. Se omiten los nombres del intervalo que no tienen una lista de visualización asociada. Si el *intervalo* es cero, no sucede nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





