---
title: función glPixelMapusv (GL. h)
description: La función glPixelMapusv configura mapas de transferencia de píxeles.
ms.assetid: c542a1be-8fb0-4269-afc0-459182c89534
keywords:
- glPixelMapusv (función) OpenGL
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
ms.openlocfilehash: 0dd4adc50af4a4168d14ac2e39d465ace360ccbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665975"
---
# <a name="glpixelmapusv-function"></a>glPixelMapusv función)

La función **glPixelMapusv** configura mapas de transferencia de píxeles.

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

Un nombre de asignación simbólico. Las diez asignaciones son las siguientes.



| Value                                                                                                                                                                               | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**\_ \_ mapa de píxeles \_ \_ de \_ Contabilidad**</dt> </dl> | Asigna índices de color a los índices de color.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**\_ \_ asignación de píxeles \_ de GL s \_ a \_ s**</dt> </dl> | Asigna los índices de estarcido a los índices de estarcido.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ R**</dt> </dl> | Asigna índices de color a componentes rojos.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ G**</dt> </dl> | Asigna índices de color a componentes verdes.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de GL I \_ a \_ B**</dt> </dl> | Asigna índices de color a los componentes azules.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**\_mapa de \_ píxeles \_ \_ de \_ Contabilidad**</dt> </dl> | Asigna índices de color a componentes alfa.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de GL R \_ a \_ r**</dt> </dl> | Asigna componentes rojos a componentes rojos.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de GL G \_ a \_ g**</dt> </dl> | Asigna los componentes verdes a los componentes verdes.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**\_ \_ mapa de píxeles \_ de contabilidad B \_ a \_ b**</dt> </dl> | Asigna componentes azules a componentes azules.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**\_ \_ \_ la asignación de píxeles de GL \_ a a \_**</dt> </dl> | Asigna los componentes alfa a los componentes alfa.<br/> |



 

</dd> <dt>

*asignar* 
</dt> <dd>

Tamaño del mapa que se está definiendo.

</dd> <dt>

*Valores* 
</dt> <dd>

Matriz de valores de *asignación* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | la *asignación* no era un valor aceptado.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el valor de la asignación *es negativo* o mayor que el de la tabla de mapa de píxeles de contabilidad \_ \_ \_ . <br/>                                                                                                                                                   |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *map era el* mapa de píxeles de contabilidad \_ \_ \_ i \_ a \_ i, el \_ mapa de píxeles de GL \_ \_ s \_ a \_ s, el mapa de píxeles de GL \_ \_ \_ i \_ a \_ R, \_ el mapa de píxeles de GL \_ \_ i \_ a \_ G, el mapa de \_ píxeles de GL \_ \_ i \_ a \_ B o \_ el mapa de píxeles de GL \_ \_ i a a \_ , y la asignación \_ no era una potencia de dos.  <br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Observaciones

La función **glPixelMap** configura las tablas de traducción, o *asignaciones*, utilizadas [**por glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D**](gltexsubimage2d.md). El uso de estas asignaciones se describe completamente en el tema [**glPixelTransfer**](glpixeltransfer.md) y, en parte, en los temas para los comandos píxel y imagen de textura. En este tema solo se describe la especificación de las asignaciones.

El parámetro de *asignación* es un nombre de mapa simbólico, que indica una de las diez asignaciones que se van a establecer. El *parámetro de asignación especifica* el número de entradas en el mapa y *los valores* son un puntero a una matriz de valores de mapa de *asignaciones* .

Las entradas de un mapa se pueden especificar como números de punto flotante de precisión sencilla, enteros cortos sin signo o enteros largos sin signo. Asignaciones que almacenan los valores de los componentes de color (todos los elementos, pero el mapa de píxeles de contabilidad \_ \_ \_ i y los mapas de píxeles de libro de contabilidad \_ \_ \_ \_ \_ \_ a \_ s) conservan sus valores en formato de punto flotante, con un tamaño no especificado de la mantisa y el exponente. Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente al formato de punto flotante interno de estas asignaciones y, a continuación, se fijan en el intervalo \[ 0, 1 \] . Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** se convierten linealmente de forma que el entero más grande que se puede representar se asigna a 1,0 y cero se asigna a 0,0.

Asignaciones que almacenan índices, \_ \_ el mapa de píxeles de contabilidad \_ i \_ \_ y \_ los mapas de píxeles de contabilidad de \_ \_ \_ la serie s a \_ s, conservan sus valores en formato de punto fijo, con un número no especificado de bits a la derecha del punto binario. Los valores de punto flotante especificados por [**glPixelMapfv**](glpixelmap.md) se convierten directamente en el formato de punto fijo interno de estas asignaciones. Los valores enteros sin signo especificados por **glPixelMapusv** y **glPixelMapuiv** especifican valores enteros, con todos los ceros a la derecha del punto binario.

En la tabla siguiente se muestran los tamaños iniciales y los valores de cada uno de los mapas. Los mapas que se indexan mediante índices de color o de estarcido deben tener el *asignador* = 2 ^ *n* para algunos *n* o los resultados no están definidos. El tamaño máximo permitido para cada mapa depende de la implementación y se puede determinar mediante una llamada a **glGet** con la \_ tabla de mapa de píxeles Max Max argument \_ \_ \_ . El máximo único se aplica a todos los mapas y es al menos 32.



| Map                      | Índice de búsqueda  | Valor de búsqueda  | Tamaño inicial | Valor inicial |
|--------------------------|---------------|---------------|--------------|---------------|
| \_ \_ mapa de píxeles \_ \_ de \_ Contabilidad | Índice de color   | Índice de color   | 1            | 0,0           |
| \_ \_ asignación de píxeles \_ de GL s \_ a \_ s | Índice de estarcido | Índice de estarcido | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de GL I \_ a \_ R | Índice de color   | R             | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de GL I \_ a \_ G | Índice de color   | G             | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de GL I \_ a \_ B | Índice de color   | B             | 1            | 0,0           |
| \_mapa de \_ píxeles \_ \_ de \_ Contabilidad | Índice de color   | A             | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de GL R \_ a \_ r | R             | R             | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de GL G \_ a \_ g | G             | G             | 1            | 0,0           |
| \_ \_ mapa de píxeles \_ de contabilidad B \_ a \_ b | B             | B             | 1            | 0,0           |
| \_ \_ \_ la asignación de píxeles de GL \_ a a \_ | A             | A             | 1            | 0,0           |



 

Las siguientes funciones recuperan información relacionada con **glPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ \_ \_ \_ \_ el argumento de mapa de píxeles de contabilidad

**glGet** con el argumento de asignación de píxeles de contabilidad de argumentos \_ \_ \_ \_ a \_ \_ tamaño s

**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ tamaño de R \_

**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ I \_ a \_ G \_

**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ B \_

**glGet** con el argumento de \_ la asignación de píxeles de GL \_ \_ I \_ a \_ un \_ tamaño

**glGet** con el argumento de la asignación de píxeles de contabilidad \_ \_ \_ r \_ a \_ \_ tamaño r

**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ G \_ a \_ g \_

**glGet** con el tamaño de la asignación de píxeles de contabilidad de argumento \_ \_ \_ b \_ a \_ B \_

**glGet** con el argumento GL de \_ píxel de \_ \_ la asignación \_ a a \_ un \_ tamaño

**glGet** con el argumento \_ \_ tabla de \_ mapa de píxeles máx. \_

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

 

 





