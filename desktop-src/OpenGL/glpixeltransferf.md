---
title: Función glPixelTransferf (Gl.h)
description: Las funciones glPixelTransferf y glPixelTransferi establecen modos de transferencia de píxeles. | Función glPixelTransferf (Gl.h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- Función glPixelTransferf OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2268147511a40aaf70a928c77b177f76870e65a7f40da4f2c6bf9428f67db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358575"
---
# <a name="glpixeltransferf-function"></a>Función glPixelTransferf

Las **funciones glPixelTransferf** [**y glPixelTransferi**](glpixeltransferi.md) establecen modos de transferencia de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Nombre simbólico del parámetro de transferencia de píxeles que se va a establecer. En la tabla siguiente se proporciona el tipo, el valor inicial y el intervalo de valores válidos para cada uno de los parámetros de transferencia de píxeles que se establecen **con glPixelTransfer**.



| Pname             | Tipo    | Valor inicial  | Intervalo válido  |
|-------------------|---------|----------------|--------------|
| COLOR \_ DE MAPA \_ GL    | Boolean | false          | true/false   |
| GALERÍA DE \_ SÍMBOLOS DE MAPA DE \_ GL  | Boolean | false          | true/false   |
| GL \_ INDEX \_ SHIFT  | integer | 0              | (8,8)        |
| GL \_ INDEX \_ OFFSET | integer | 0              | (8,8)        |
| GL \_ RED \_ SCALE    | integer | 1.0            | (8,8)        |
| GL \_ GREEN \_ SCALE  | FLOAT   | 1.0            | (8,8)        |
| GL \_ BLUE \_ SCALE   | FLOAT   | 1.0            | (8,8)        |
| GL \_ ALPHA \_ SCALE  | FLOAT   | 1.0            | (8,8)        |
| ESCALA \_ DE PROFUNDIDAD DE \_ GL  | FLOAT   | 1.0            | (8,8)        |
| GL \_ RED \_ BIAS     | FLOAT   | 0,0            | (8,8)        |
| GL \_ GREEN \_ BIAS   | FLOAT   | 0,0            | (8,8)        |
| GL \_ BLUE \_ BIAS    | FLOAT   | 0,0            | (8,8)        |
| GL \_ ALPHA \_ BIAS   | FLOAT   | 0,0            | (8,8)        |
| \_SESGO DE PROFUNDIDAD DE \_ GL   | FLOAT   | 0,0            | (8,8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor en el que se establece *pname.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La función **glPixelTransfer** establece modos de transferencia de píxeles que afectan al funcionamiento de [**posteriores glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D,**](glcopytexsubimage1d.md) [**glCopyTexSubImage2D,**](glcopytexsubimage2d.md) [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D.**](gltexsubimage2d.md) Los algoritmos especificados por los modos de transferencia de píxeles funcionan en píxeles después de leerse desde el búfer de **fotogramas (glReadPixels** y **glCopyPixels)** o desempaquetados de la memoria de cliente **(glDrawPixels,** **glTexImage1D** y **glTexImage2D).** Las operaciones de transferencia de píxeles se realizaron en el mismo orden y de la misma manera, independientemente del comando que dio lugar a la operación de píxeles. Los modos de almacenamiento de píxeles [**(glPixelStore)**](glpixelstore-functions.md)controlan el desempaquete de píxeles que se leen de la memoria del cliente y el empaquetado de píxeles que se escriben de nuevo en la memoria del cliente.

Las operaciones de transferencia de píxeles controlan cuatro tipos de píxeles fundamentales: *color,* *índice de color,* *profundidad* y galería *de símbolos.* Los píxeles de color están hechos de cuatro valores de punto flotante con tamaños de mantisa y exponente no especificados, escalados de forma que 0,0 representa la intensidad cero y 1,0 representa la intensidad completa. Los índices de color constan de un único valor de punto fijo, con precisión no especificada a la derecha del punto binario. Los píxeles de profundidad componen un único valor de punto flotante, con tamaños de mantisa y exponente no especificados, escalado de forma que 0,0 representa el valor de búfer de profundidad mínimo y 1,0 representa el valor de búfer de profundidad máximo. Por último, los píxeles de galería de símbolos comprenden un único valor de punto fijo, con precisión no especificada a la derecha del punto binario.

Las operaciones de transferencia de píxeles realizadas en los cuatro tipos de píxeles básicos son las siguientes:



| Tipo de píxel  | Operación de transferencia de píxeles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Cada uno de los cuatro componentes de color se multiplica por un factor de escala y, a continuación, se agrega a un factor de sesgo. Es decir, el componente rojo se multiplica por GL RED SCALE y, a continuación, se agrega a GL RED BIAS; el componente verde se multiplica por GL GREEN SCALE y, a continuación, se agrega a GL GREEN BIAS; el componente azul se multiplica por GL BLUE SCALE y, a continuación, se agrega a GL BLUE BIAS; y el componente alfa se multiplica por GL ALPHA SCALE y, a continuación, se agrega a \_ \_ GL \_ \_ \_ \_ ALPHA \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ BIAS. Una vez escalados y sesgados los cuatro componentes de color, cada uno se fija al intervalo \[ 0,1. \] Todos los valores de escala de colores y sesgo se especifican **con glPixelTransfer.** <br/> Si GL MAP COLOR es true, cada componente de color se escala por el tamaño del mapa de color a color correspondiente y, a continuación, se reemplaza por el contenido de ese mapa indexado por el componente \_ \_ escalado. Es decir, el componente rojo se escala mediante GL PIXEL MAP R TO R SIZE y, a continuación, se reemplaza por el contenido de \_ GL PIXEL MAP R TO \_ \_ R \_ \_ \_ \_ \_ \_ \_ \_ indexado por sí mismo. El componente verde se escala mediante GL PIXEL MAP G TO G SIZE y, a continuación, se reemplaza por el contenido de \_ GL PIXEL MAP G TO \_ \_ G \_ \_ \_ \_ \_ \_ \_ \_ indexado por sí mismo. El componente azul se escala mediante GL PIXEL MAP B TO B SIZE y, a continuación, se reemplaza por el contenido de \_ GL PIXEL MAP B TO \_ \_ B \_ \_ \_ \_ \_ \_ \_ \_ indexado por sí mismo. El componente alfa se escala mediante GL PIXEL MAP A TO A SIZE y, a continuación, se reemplaza por el contenido de \_ GL PIXEL MAP A TO \_ \_ A \_ \_ \_ \_ \_ \_ \_ \_ indexado por sí mismo. A continuación, todos los componentes tomados de los mapas se fijan en el \[ intervalo 0,1. \] GL \_ MAP COLOR se especifica con \_ **glPixelTransfer.** El contenido de los distintos mapas se especifica con **glPixelMap.**<br/>                                                                                                                        |
| Índice de color | Cada índice de color se desplaza a la izquierda por los bits GL INDEX SHIFT, rellenando con ceros cualquier bit más allá del número de bits de fracción que lleva el índice \_ \_ de punto fijo. Si GL \_ INDEX \_ SHIFT es negativo, el desplazamiento se desplaza a la derecha y, de nuevo, se rellena cero. A \_ continuación, se agrega GL INDEX \_ OFFSET al índice. GL \_ INDEX SHIFT y GL INDEX OFFSET se especifican con \_ \_ \_ **glPixelTransfer.**<br/> Desde este punto, la operación difiere en función del formato necesario de los píxeles resultantes. Si los píxeles resultantes se van a escribir en un búfer de índice de color o si se leen de nuevo en la memoria del cliente en formato GL COLOR INDEX, los píxeles se seguirán tratando como \_ \_ índices. Si GL MAP COLOR es true, cada índice se enmascara por \_ \_ 2 ^ *n* 1, donde *n* es GL PIXEL MAP I TO I SIZE y, a continuación, se reemplaza por el contenido de GL PIXEL MAP I TO I indexado por el \_ \_ \_ \_ valor \_ \_ \_ \_ \_ \_ \_ enmascarado. GL \_ MAP COLOR se especifica con \_ **glPixelTransfer.** El contenido del mapa de índice se especifica con **glPixelMap**.<br/> Si los píxeles resultantes se van a escribir en un búfer de color RGBA, o si se van a volver a leer en la memoria del cliente en un formato distinto de GL COLOR INDEX, los píxeles se convierten de índices a colores haciendo referencia a los cuatro mapas GL \_ PIXEL MAP I TO \_ \_ \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B y \_ GL PIXEL MAP I \_ \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ A. Antes de desreferenciar, el índice se enmascara en 2 n 1, donde n es GL PIXEL MAP I TO R SIZE para el mapa rojo, GL PIXEL MAP I TO G SIZE para el mapa \_ \_ \_ \_ \_ \_ \_ verde, GL PIXEL MAP I TO B \_ \_ SIZE \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ para el mapa azul y GL PIXEL MAP I TO A SIZE para el mapa alfa. A continuación, todos los componentes tomados de los mapas se fijan en el \[ intervalo 0,1. \] El contenido de los cuatro mapas se especifica con **glPixelMap**.<br/> |
| Profundidad       | Cada valor de profundidad se multiplica por GL DEPTH SCALE, se agrega a GL DEPTH BIAS y, a continuación, se fija al \_ \_ intervalo \_ \_ \[ 0,1. \]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Cada índice se desplaza en bits GL INDEX SHIFT igual que un índice de color y, a continuación, se agrega \_ \_ a GL INDEX \_ \_ OFFSET. Si GL MAP STENCIL es true, cada índice se enmascara por \_ \_ 2n 1, donde *n* es GL PIXEL MAP S TO S SIZE y, a continuación, se reemplaza por el contenido de GL PIXEL MAP S TO S indexado por el \_ \_ \_ \_ valor \_ \_ \_ \_ \_ \_ \_ enmascarado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La [**función glPixelTransferf**](glpixeltransfer.md) se puede usar para establecer cualquier parámetro de transferencia de píxeles. Si el tipo de parámetro es booleano, 0,0 implica false y cualquier otro valor implica true. Si *pname* es un parámetro entero, *param* se redondea al entero más cercano.

Del mismo modo, **glPixelTransferi** también se puede usar para establecer cualquiera de los parámetros de transferencia de píxeles. Los parámetros booleanos se establecen en false si *param* es 0 y true en caso contrario. El *parámetro param* se convierte en punto flotante antes de asignarse a parámetros con valores reales.

Si un comando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels,**](glreadpixels.md) [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)o [**glTexImage2D**](glteximage2d.md) se coloca en una lista de visualización (vea [**glNewList**](glnewlist.md) y [**glCallList),**](glcalllist.md)la configuración del modo de transferencia de píxeles en vigor cuando se ejecuta la lista de visualización son las que se usan.  Pueden ser diferentes de la configuración cuando el comando se compiló en la lista de visualización.

Las siguientes funciones recuperan información relacionada con **glPixelTransfer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP \_ COLOR

**glGet con** el argumento GL \_ MAP \_ STENCIL

**glGet con** el argumento GL \_ INDEX \_ SHIFT

**glGet con** el argumento GL \_ INDEX \_ OFFSET

**glGet con** el argumento GL \_ RED \_ SCALE

**glGet con** el argumento GL \_ RED \_ BIAS

**glGet con** el argumento GL \_ GREEN \_ SCALE

**glGet con** el argumento GL \_ GREEN \_ BIAS

**glGet con** el argumento GL \_ BLUE \_ SCALE

**glGet con** el argumento GL \_ BLUE \_ BIAS

**glGet con** el argumento GL \_ ALPHA \_ SCALE

**glGet con** el argumento GL \_ ALPHA \_ BIAS

**glGet con** el argumento GL \_ DEPTH \_ SCALE

**glGet con** el argumento GL \_ DEPTH \_ BIAS

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





