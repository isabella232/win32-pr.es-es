---
title: Función glListBase (Gl.h)
description: La función glListBase establece la base de la lista de presentación para glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- Función glListBase OpenGL
topic_type:
- apiref
api_name:
- glListBase
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba7cbe7b179184efa739ac3492f4e74b36f56abe0f02498a0e1a688b85183a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938522"
---
# <a name="gllistbase-function"></a>función glListBase

La **función glListBase** establece la base de la lista de presentación **para glCallLists.**

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glListBase(
   GLuint base
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*base* 
</dt> <dd>

Desplazamiento entero que se agregará a [**los desplazamientos glCallLists**](glcalllists.md) para generar nombres de lista para mostrar. El valor inicial es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glListBase** especifica una matriz de desplazamientos. Los nombres de lista para mostrar se generan *agregando base a* cada desplazamiento. Se ejecutan nombres que hacen referencia a listas para mostrar válidas; Otros se omiten.

La función siguiente recupera información relacionada con **glListBase**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ LIST \_ BASE

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





