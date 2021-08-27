---
title: Función glDeleteLists (Gl.h)
description: La función glDeleteLists elimina un grupo contiguo de listas para mostrar.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- Función glDeleteLists OpenGL
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
ms.openlocfilehash: 6ec0ffac68119f6f2080ef6ca96ec63fbd35176d3541464a89b6c31f4941b4c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081665"
---
# <a name="gldeletelists-function"></a>Función glDeleteLists

La **función glDeleteLists** elimina un grupo contiguo de listas para mostrar.

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

Nombre entero de la primera lista para mostrar que se eliminará.

</dd> <dt>

*range* 
</dt> <dd>

Número de listas para mostrar que se eliminarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *el intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glDeleteLists** hace que se elimine un grupo contiguo de listas para mostrar. El *parámetro list* es el nombre de la primera lista para mostrar que se va a eliminar y *el* intervalo es el número de listas para mostrar que se van a eliminar. Se eliminan todas las *listas para mostrar d* con *el* intervalo de  =    =  *lista*  +  *d :* 1.

Se liberan todas las ubicaciones de almacenamiento asignadas a las listas de presentación especificadas y los nombres están disponibles para su reutilización más adelante. Los nombres dentro del intervalo que no tienen una lista de visualización asociada se omiten. Si *range* es cero, no ocurre nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





