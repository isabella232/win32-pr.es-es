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
ms.openlocfilehash: c46af03477afc1b656df3a321fd8aa652b034b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253791"
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



## <a name="remarks"></a>Observaciones

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





