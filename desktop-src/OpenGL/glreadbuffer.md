---
title: función glReadBuffer (GL. h)
description: La función glReadBuffer selecciona un origen de búfer de color para los píxeles.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686116"
---
# <a name="glreadbuffer-function"></a>glReadBuffer función)

La función **glReadBuffer** selecciona un origen de búfer de color para los píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Un búfer de color. Los valores aceptados son GL \_ Front \_ left, GL \_ Front \_ right, GL \_ back \_ left, GL back Right, GL Front, GL up, GL \_ \_ \_ \_ \_ left, GL \_ right y GL \_ AUX *i*, donde *i* está entre 0 y \_ búferes auxiliares de GL \_ 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era uno de los doce (o más) valores aceptados.<br/>                                                             |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *modo* especificó un búfer que no existe.<br/>                                                                             |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glReadBuffer** especifica un búfer de color como el origen de los siguientes comandos [**glReadPixels**](glreadpixels.md) y [**glCopyPixels**](glcopypixels.md) . El parámetro de *modo* acepta uno de doce valores predefinidos o más. (GL \_ ) \_Siempre se definen AUX0 a GL AUX3). En un sistema completamente configurado, GL \_ Front, GL \_ left y GL \_ Front \_ left, todo el nombre del búfer de la izquierda, la \_ parte delantera derecha y el nombre de la contabilidad de la derecha el búfer de la derecha, y el nombre de contabilidad de la izquierda \_ \_ y la parte posterior \_ \_ \_ del búfer de retroceso.

Las configuraciones de búfer doble no estéreo tienen solo un búfer de la izquierda y la derecha. Las configuraciones de un solo búfer tienen un búfer de front-end y front-Right si es estéreo, y solo un búfer de Front-Left si es no estéreo. Es un error especificar un búfer inexistente para **glReadBuffer**.

De forma predeterminada, el *modo* está \_ en la parte frontal de la contabilidad en configuraciones de búfer único y \_ en las configuraciones de búfer doble.

La siguiente función recupera información relacionada con **glReadBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ búfer de lectura de GL \_

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





