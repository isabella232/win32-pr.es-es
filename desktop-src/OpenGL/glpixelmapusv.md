---
title: Función glPixelMapusv (Gl.h)
description: La función glPixelMapusv configura mapas de transferencia de píxeles.
ms.assetid: c542a1be-8fb0-4269-afc0-459182c89534
keywords:
- Función glPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf5d49f87e32de2a11dff5aef3c1220f0fd4d45d7333f9e0aeff9766da53d69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128095"
---
# <a name="glpixelmapusv-function"></a>Función glPixelMapusv

La **función glPixelMapusv** configura mapas de transferencia de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelMapusv(
         GLenum   map,
         GLsizei  mapsize,
   const GLushort *values
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*map* 
</dt> <dd>

Nombre de mapa simbólico. Los diez mapas son los siguientes.



| Value                                                                                                                                                                               | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ I**</dt> </dl> | Mapas índices de color a índices de color.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ S \_ TO \_ S**</dt> </dl> | Mapas de galería de símbolos a índices de galería de símbolos.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ R**</dt> </dl> | Mapas índices de color a componentes rojos.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ G**</dt> </dl> | Mapas índices de color a componentes verdes.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ B**</dt> </dl> | Mapas índices de color a componentes azules.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ A**</dt> </dl> | Mapas índices de color a componentes alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ R \_ TO \_ R**</dt> </dl> | Mapas componentes rojos a componentes rojos.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ G \_ TO \_ G**</dt> </dl> | Mapas componentes verdes a componentes verdes.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ B \_ TO \_ B**</dt> </dl> | Mapas componentes azules a componentes azules.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**ASIGNACIÓN \_ \_ DE PÍXELES DE GL \_ A \_ \_ A**</dt> </dl> | Mapas componentes alfa a componentes alfa.<br/> |



 

</dd> <dt>

*mapsize* 
</dt> <dd>

Tamaño del mapa que se va a definir.

</dd> <dt>

*Valores* 
</dt> <dd>

Matriz de *valores de asignación.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *map* no era un valor aceptado.<br/>                                                                                                                                                                                |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *mapsize* era negativo o mayor que GL \_ PIXEL \_ MAP \_ TABLE. <br/>                                                                                                                                                   |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *map* was GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP \_ S TO \_ \_ \_ \_ S, GL PIXEL MAP \_ I TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ \_ G, GL PIXEL MAP \_ I TO B o GL PIXEL MAP I \_ TO \_ \_ \_ \_ \_ \_ \_ \_ A, and *mapsize* was not a power of two. <br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Comentarios

La función **glPixelMap** configura tablas de traducción, o *mapas,* usadas por [**glCopyPixels,**](glcopypixels.md) [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D,**](glcopytexsubimage1d.md) [**glCopyTexSubImage2D,**](glcopytexsubimage2d.md) [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D.**](gltexsubimage2d.md) El uso de estos mapas se describe completamente en el tema [**glPixelTransfer**](glpixeltransfer.md) y, en parte, en los temas de los comandos de imagen de textura y píxeles. En este tema solo se describe la especificación de los mapas.

El *parámetro map* es un nombre de mapa simbólico, que indica uno de los diez mapas que se establecerán. El *parámetro mapsize* especifica el número de entradas del mapa y *values* es un puntero a una matriz de valores *de asignación* de mapa.

Las entradas de un mapa se pueden especificar como números de punto flotante de precisión sencilla, enteros cortos sin signo o enteros largos sin signo. Mapas que almacenan valores de componente de color (todos menos GL PIXEL MAP I TO I y GL PIXEL MAP S TO S) conservan sus valores en formato de punto flotante, con tamaños de mantisa y exponente no \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ especificados. Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente al formato de punto flotante interno de estos mapas y, a continuación, se fijan en el \[ intervalo 0,1 \] . Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** se convierten linealmente de forma que el entero representable más grande se asigna a 1,0 y cero se asigna a 0,0.

Mapas que almacenan índices, GL PIXEL MAP I TO I y GL PIXEL MAP S TO S, conservan sus valores en formato de punto fijo, con un número no especificado de bits a la derecha del \_ \_ punto \_ \_ \_ \_ \_ \_ \_ \_ binario. Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente al formato de punto fijo interno de estos mapas. Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** especifican valores enteros, con todos los ceros a la derecha del punto binario.

En la tabla siguiente se muestran los tamaños y valores iniciales de cada uno de los mapas. Mapas indexados por índices de color o galería de símbolos deben tener *mapsize* = 2 ^ *n* para *algunos n* o los resultados no están definidos. El tamaño máximo permitido para cada mapa depende de la implementación y se puede determinar mediante una llamada **a glGet** con el argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE. El único máximo se aplica a todos los mapas y es al menos 32.



| Asignación                      | Índice de búsqueda  | Valor de búsqueda  | Tamaño inicial | Valor inicial |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ I | índice de color   | índice de color   | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ S \_ TO \_ S | índice de galería de símbolos | índice de galería de símbolos | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ R | índice de color   | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ G | índice de color   | G             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ B | índice de color   | B             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ A | índice de color   | A             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ R \_ TO \_ R | R             | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ G \_ TO \_ G | G             | G             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ B \_ TO \_ B | B             | B             | 1            | 0,0           |
| ASIGNACIÓN \_ \_ DE PÍXELES DE GL \_ A \_ \_ A | A             | A             | 1            | 0,0           |



 

Las funciones siguientes recuperan información relacionada **con glPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





