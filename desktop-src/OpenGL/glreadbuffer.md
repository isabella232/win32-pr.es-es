---
title: Función glReadBuffer (Gl.h)
description: La función glReadBuffer selecciona un origen de búfer de color para píxeles.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- Función glReadBuffer OpenGL
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
ms.openlocfilehash: 3a25e9a799185b1a509510abb81617895fbbd0624d8816110e4c2ba8e4a7c1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937955"
---
# <a name="glreadbuffer-function"></a>función glReadBuffer

La **función glReadBuffer** selecciona un origen de búfer de color para píxeles.

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

Búfer de color. Los valores aceptados son GL \_ FRONT \_ LEFT, GL \_ FRONT \_ RIGHT, GL BACK \_ \_ \_ LEFT, GL BACK \_ RIGHT, GL \_ FRONT, GL BACK, GL LEFT, GL RIGHT y GL AUX i , donde i está entre 0 y \_ \_ GL AUX \_ \_   \_ \_ BUFFERS 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el* modo no era uno de los doce (o más) valores aceptados.<br/>                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *el* modo especificó un búfer que no existe.<br/>                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glReadBuffer** especifica un búfer de color como origen para los siguientes comandos [**glReadPixels**](glreadpixels.md) y [**glCopyPixels.**](glcopypixels.md) El *parámetro* mode acepta uno de los doce o más valores predefinidos. (GL) \_ Siempre se definen DESDE AUX0 hasta \_ GL AUX3). En un sistema completamente configurado, GL FRONT, GL LEFT y GL FRONT LEFT, todo el nombre del búfer de la izquierda, GL FRONT RIGHT y GL RIGHT el búfer de \_ \_ \_ \_ \_ \_ \_ front-right, y GL \_ BACK \_ LEFT \_ y GL BACK el búfer de la parte posterior izquierda.

Las configuraciones que no son de almacenamiento en búfer doble tienen solo un búfer front-left y un búfer de back-left. Las configuraciones de un solo búfer tienen un búfer front-left y un búfer de front-right si son estéreo, y solo un búfer de front-left si no son destereo. Es un error especificar un búfer inexistente en **glReadBuffer.**

De forma predeterminada, *el modo* es GL FRONT en configuraciones de un solo búfer y GL BACK \_ en \_ configuraciones de doble búfer.

La función siguiente recupera información relacionada con **glReadBuffer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ READ \_ BUFFER

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





