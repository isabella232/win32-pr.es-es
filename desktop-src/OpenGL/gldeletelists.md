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
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362080"
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

Número de listas de visualización que se eliminarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *el intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glDeleteLists** hace que se elimine un grupo contiguo de listas para mostrar. El *parámetro* list es el nombre de la primera lista para mostrar que se va a eliminar y *el* intervalo es el número de listas para mostrar que se van a eliminar. Se eliminan todas las *listas de* visualización d *con el* intervalo de lista d de la lista d :  =    =    +   1.

Se liberan todas las ubicaciones de almacenamiento asignadas a las listas de presentación especificadas y los nombres están disponibles para reutilizarse más adelante. Los nombres dentro del intervalo que no tienen una lista de presentación asociada se omiten. Si *el intervalo* es cero, no ocurre nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





