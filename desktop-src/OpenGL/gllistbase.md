---
title: función glListBase (GL. h)
description: La función glListBase establece la base de la lista de visualización para glCallLists.
ms.assetid: df82f699-b2af-471a-83f3-5620857ba45d
keywords:
- glListBase (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996041"
---
# <a name="gllistbase-function"></a>glListBase función)

La función **glListBase** establece la base de la lista de visualización para **glCallLists**.

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

Desplazamiento de entero que se agregará a los desplazamientos de [**glCallLists**](glcalllists.md) para generar nombres de lista de presentación. El valor inicial es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glListBase** especifica una matriz de desplazamientos. Los nombres de lista de visualización se generan agregando *base* a cada desplazamiento. Se ejecutan los nombres que hacen referencia a listas de presentación válidas; otros se omiten.

La siguiente función recupera información relacionada con **glListBase**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento base de la lista de contabilidad \_ \_

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

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





