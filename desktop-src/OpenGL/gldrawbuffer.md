---
title: Función glDrawBuffer (Gl.h)
description: La función glDrawBuffer especifica en qué búferes de color se van a dibujar.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- Función glDrawBuffer OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362067"
---
# <a name="gldrawbuffer-function"></a>Función glDrawBuffer

La **función glDrawBuffer** especifica en qué búferes de color se van a dibujar.

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

Especifica hasta cuatro búferes de color en los que se va a dibujar con las siguientes constantes simbólicas aceptables.



| Value                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ NONE**</dt> </dl>                                 | No se escriben búferes de color.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ FRONT \_ LEFT**</dt> </dl>              | Solo se escribe el búfer de color de la parte izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ FRONT \_ RIGHT**</dt> </dl>           | Solo se escribe el búfer de color front-right.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ BACK \_ LEFT**</dt> </dl>                 | Solo se escribe el búfer de color de la parte izquierda.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ BACK \_ RIGHT**</dt> </dl>              | Solo se escribe el búfer de color de la parte posterior derecha.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ FRONT**</dt> </dl>                              | Solo se escriben los búferes de color front-left y front-right. Si no hay ningún búfer de color front-right, solo se escribe el búfer de color izquierdo.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ BACK**</dt> </dl>                                 | Solo se escriben los búferes de color hacia atrás a la izquierda y hacia atrás a la derecha. Si no hay ningún búfer de color de la parte posterior derecha, solo se escribe el búfer de color de la parte posterior izquierda.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ LEFT**</dt> </dl>                                 | Solo se escriben los búferes de color front-left y back-left. Si no hay ningún búfer de color hacia atrás a la izquierda, solo se escribe el búfer de color de la parte izquierda.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**DERECHA \_ DE GL**</dt> </dl>                              | Solo se escriben los búferes de color front-right y back-right. Si no hay ningún búfer de color de la parte posterior derecha, solo se escribe el búfer de color de la parte derecha.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ FRONT \_ AND \_ BACK**</dt> </dl> | Se escriben todos los búferes de color frontal y posterior (front-left, front-right, back-left, back-right). Si no hay búferes de color de reserva, solo se escriben los búferes de color front-left y front-right. Si no hay búferes de color derecho, solo se escriben los búferes de color de la parte izquierda y de la parte posterior izquierda. Si no hay búferes de color derecho o posterior, solo se escribe el búfer de color de la parte izquierda.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | Solo se escribe el búfer de color *auxiliar i;* *i* está entre 0 y GL \_ AUX \_ BUFFERS - 1. (GL) \_ BUFFERS DE AUX \_ no es el límite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar el número de búferes auxiliares disponibles).<br/>                                                                                                                            |



 

El valor predeterminado es GL FRONT para contextos de búfer único \_ y GL BACK para \_ contextos de doble búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *mode* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | No existía ninguno de los búferes indicados *por el* modo.<br/>                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Observaciones

Cuando los colores se escriben en el búfer de fotogramas, se escriben en los búferes de color especificados por **glDrawBuffer.**

Si se selecciona más de un búfer de color para dibujar, las operaciones lógicas o de combinación se calculan y se aplican de forma independiente para cada búfer de color y pueden producir resultados diferentes en cada búfer.

Los contextos monográficos incluyen solo búferes izquierdos, y los contextos estereográficos incluyen búferes izquierdo y derecho. Del mismo modo, los contextos de un solo búfer incluyen solo búferes front-buffer y los contextos de doble búfer incluyen búferes front-and-back. El contexto se selecciona en la inicialización de OpenGL.

Siempre es el caso de GL \_ AUX *i* = GL \_ AUX0 + *i*.

Las funciones siguientes recuperan información relacionada con la **función glDrawBuffer:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ DRAW \_ BUFFER

**glGet con** el argumento GL \_ AUX \_ BUFFERS

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

 

 





