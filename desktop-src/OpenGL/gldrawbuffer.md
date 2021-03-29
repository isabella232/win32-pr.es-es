---
title: función glDrawBuffer (GL. h)
description: La función glDrawBuffer especifica en qué búferes de color se van a dibujar.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665949"
---
# <a name="gldrawbuffer-function"></a>glDrawBuffer función)

La función **glDrawBuffer** especifica en qué búferes de color se van a dibujar.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Especifica hasta cuatro búferes de color en los que se van a dibujar con las siguientes constantes simbólicas aceptables.



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ ninguno**</dt> </dl>                                 | No se escriben búferes de color.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**en la \_ parte frontal \_ izquierda**</dt> </dl>              | Solo se escribe el búfer de color Front-Left.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**lado \_ derecho de contabilidad \_**</dt> </dl>           | Solo se escribe el búfer de color Front-Right.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**LIBRO de \_ fondo hacia la \_ izquierda**</dt> </dl>                 | Solo se escribe el búfer de color de la izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**\_derecha atrás \_**</dt> </dl>              | Solo se escribe el búfer de color de la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**frontal de GL \_**</dt> </dl>                              | Solo se escriben los búferes de color Front-Left y front-Right. Si no hay ningún búfer de colores delante de la derecha, solo se escribe el búfer de color izquierdo frontal.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**libro \_ de contabilidad**</dt> </dl>                                 | Solo se escriben los búferes de color de la izquierda y la derecha. Si no hay ningún búfer de color de fondo derecho, solo se escribe el búfer de color de fondo izquierdo.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**libro de contabilidad \_ izquierda**</dt> </dl>                                 | Solo se escriben los búferes de color Front-Left y back-Left. Si no hay ningún búfer de color de fondo izquierdo, solo se escribe el búfer de color Front-Left.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**libro de contabilidad \_ derecha**</dt> </dl>                              | Solo se escriben los búferes de color de la derecha y la derecha. Si no hay ningún búfer de color de fondo derecho, solo se escribe el búfer de color de la derecha.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**\_anverso \_ y \_ atrás de GL**</dt> </dl> | Se escriben todos los búferes de color delantero y de fondo (Front-Left, Front-Right, Back-izquierda, hacia la derecha). Si no hay ningún búfer de color de fondo, solo se escriben los búferes de color Front-Left y front-Right. Si no hay ningún búfer de color a la derecha, solo se escriben los búferes de color Front-Left y back-izquierda. Si no hay ningún búfer de color derecho o de fondo, solo se escribe el búfer de color Front-Left.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | Solo se escribe el búfer de color auxiliar *i* . *i* está entre 0 y \_ \_ búferes auxiliares de GL-1. (GL \_ ) \_Los búferes de AUX no son el límite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar el número de búferes auxiliares disponibles).<br/>                                                                                                                            |



 

El valor predeterminado es el \_ front-end para los contextos de un solo búfer y el libro \_ de reserva para los contextos de doble búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Ninguno de los búferes indicados por el *modo* existía.<br/>                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Observaciones

Cuando los colores se escriben en fotogramas, se escriben en los búferes de color especificados por **glDrawBuffer**.

Si se selecciona más de un búfer de color para dibujar, las operaciones lógicas o de mezcla se calculan y se aplican de forma independiente para cada búfer de color y pueden generar resultados diferentes en cada búfer.

Los contextos de Monoscopic incluyen solo los búferes izquierdos y los contextos de Stereoscopic incluyen los búferes izquierdo y derecho. Del mismo modo, los contextos de un solo búfer incluyen solo los búferes frontales y los contextos de búfer doble incluyen los búferes frontal y posterior. El contexto se selecciona en la inicialización de OpenGL.

Siempre es el caso de GL \_ AUX *i* = GL \_ AUX0 + *i*.

Las siguientes funciones recuperan información relacionada con la función **glDrawBuffer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de \_ búfer de dibujo de GL \_

**glGet** con \_ búferes auxiliares de contabilidad de argumentos \_

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





