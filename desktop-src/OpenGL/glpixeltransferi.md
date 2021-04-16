---
title: función glPixelTransferi (GL. h)
description: Las funciones glPixelTransferf y glPixelTransferi establecen los modos de transferencia de píxeles. | función glPixelTransferi (GL. h)
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
keywords:
- glPixelTransferi (función) OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67415a8e105dc95f3e21e6968042496b9db52038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689743"
---
# <a name="glpixeltransferi-function"></a>glPixelTransferi función)

Las funciones [**glPixelTransferf**](glpixeltransferf.md) y **glPixelTransferi** establecen los modos de transferencia de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelTransferi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PName* 
</dt> <dd>

Nombre simbólico del parámetro de transferencia de píxeles que se va a establecer. En la tabla siguiente se proporciona el tipo, el valor inicial y el intervalo de valores válidos para cada uno de los parámetros de transferencia en píxeles que se establecen con **glPixelTransfer**.



| PName             | Tipo    | Valor inicial  | Intervalo válido  |
|-------------------|---------|----------------|--------------|
| \_color del mapa de contabilidad \_    | Boolean | false          | true/false   |
| Galería de símbolos del \_ mapa de contabilidad \_  | Boolean | false          | true/false   |
| \_cambio de índice de GL \_  | integer | 0              | (8, 8)        |
| \_desplazamiento de índice de GL \_ | integer | 0              | (8, 8)        |
| \_escalado rojo de GL \_    | integer | 1,0            | (8, 8)        |
| \_escala verde de contabilidad general \_  | FLOAT   | 1,0            | (8, 8)        |
| \_escala de azul de GL \_   | FLOAT   | 1,0            | (8, 8)        |
| escala de CC \_ \_  | FLOAT   | 1,0            | (8, 8)        |
| \_escala de profundidad de GL \_  | FLOAT   | 1,0            | (8, 8)        |
| \_sesgo rojo de GL \_     | FLOAT   | 0,0            | (8, 8)        |
| \_sesgo verde de contabilidad general \_   | FLOAT   | 0,0            | (8, 8)        |
| \_sesgo azul de GL \_    | FLOAT   | 0,0            | (8, 8)        |
| \_sesgo alfa de GL \_   | FLOAT   | 0,0            | (8, 8)        |
| \_tendencia de profundidad de contabilidad \_   | FLOAT   | 0,0            | (8, 8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor que *PName* está establecido en.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glPixelTransfer** establece los modos de transferencia de píxeles que afectan al funcionamiento de los siguientes comandos [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D**](gltexsubimage2d.md) . Los algoritmos que se especifican mediante los modos de transferencia en píxeles operan en píxeles después de que se leen desde fotogramas (**glReadPixels** y **glCopyPixels**) o se desempaquetan de la memoria del cliente (**glDrawPixels**, **glTexImage1D** y **glTexImage2D**). Las operaciones de transferencia en píxeles se producen en el mismo orden y de la misma manera, independientemente del comando que haya producido la operación de píxeles. Los modos de almacenamiento en píxeles ([**glPixelStore**](glpixelstore-functions.md)) controlan el desempaquetado de los píxeles que se leen de la memoria del cliente y el empaquetado de píxeles que se escriben en la memoria del cliente.

Las operaciones de transferencia de píxeles administran cuatro tipos de píxeles fundamentales: *color*, *Índice de color*, *profundidad* y *estarcido*. Los píxeles de color se componen de cuatro valores de punto flotante con una mantisa no especificada y tamaños de exponente, escalados de tal forma que 0,0 representa la intensidad de cero y 1,0 representa intensidad total. Los índices de color componen un único valor de punto fijo, con una precisión no especificada a la derecha del punto binario. Los píxeles de profundidad comprenden un único valor de punto flotante, con un tamaño y una mantisa sin especificar, escalados de tal forma que 0,0 representa el valor del búfer de profundidad mínimo y 1,0 representa el valor del búfer de profundidad máximo. Por último, los píxeles de estarcido componen un único valor de punto fijo, con una precisión no especificada a la derecha del punto binario.

Las operaciones de transferencia de píxeles realizadas en los cuatro tipos de píxeles básicos son las siguientes:



| Tipo de píxel  | Operación de transferencia de píxeles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Cada uno de los cuatro componentes de color se multiplica por un factor de escala y, a continuación, se agrega a un factor de sesgo. Es decir, el componente rojo se multiplica por escala de rojo de contabilidad \_ \_ y, a continuación, se agrega a la diferencia de color rojo de contabilidad general \_ \_ ; el componente verde se multiplica por escala de verde de contabilidad y, a continuación, se agrega a la diferencia de verde de contabilidad general \_ \_ \_ \_ ; el componente azul se \_ \_ \_ \_ \_ \_ \_ \_ multiplica por escala de azul de contabilidad y se agrega a la diferencia alfa de contabilidad Una vez que los cuatro componentes de color se escalan y sesgan, cada uno se fija en el intervalo \[ 0, 1 \] . Todos los valores de escala de colores y de sesgo se especifican con **glPixelTransfer**. <br/> Si el \_ color del mapa \_ de contabilidad es true, cada componente de color se escala según el tamaño de la asignación de color a color correspondiente y, a continuación, se reemplaza por el contenido de la asignación indizada por el componente escalado. Es decir, el componente rojo se escala según el \_ \_ \_ tamaño de la asignación de píxeles de GL r \_ a \_ r y, a continuación, se \_ reemplaza por el contenido de la asignación de píxeles de contabilidad de \_ \_ \_ r \_ a \_ r indizada por sí misma. El componente verde se escala según el \_ \_ \_ tamaño de la asignación de píxeles de GL g \_ a \_ g \_ y, a continuación, se reemplaza por el contenido de la asignación de píxeles de GL \_ \_ \_ g \_ a \_ g indexada por sí misma. El componente azul se escala según el \_ \_ \_ \_ tamaño del mapa de píxeles de contabilidad b a \_ b y, \_ a continuación, se reemplaza por el contenido del mapa de píxeles de contabilidad \_ \_ \_ b \_ a \_ b indexado por sí mismo. El componente alfa se escala mediante el \_ \_ mapa de píxeles de contabilidad a \_ \_ \_ un \_ tamaño y, a continuación, se reemplaza por el contenido de la asignación de píxeles de GL a \_ \_ \_ \_ a \_ un indexado por sí mismo. Todos los componentes tomados de las asignaciones se fijan en el intervalo \[ 0, 1 \] . El \_ color del mapa GL \_ se especifica con **glPixelTransfer**. El contenido de las distintas asignaciones se especifica con **glPixelMap**.<br/>                                                                                                                        |
| Índice de color | Cada índice de color se desplaza a la izquierda por los \_ bits de desplazamiento de índice de contabilidad \_ , rellenando con ceros cualquier bit más allá del número de bits de fracción transportados por el índice de punto fijo. Si \_ el cambio de índice de GL \_ es negativo, el desplazamiento está a la derecha; de nuevo, se rellena con cero. \_ \_ A continuación, se agrega el desplazamiento del índice GL al índice. El \_ desplazamiento del índice GL \_ y el desplazamiento del \_ Índice GL \_ se especifican con **glPixelTransfer**.<br/> Desde este punto, la operación difiere en función del formato requerido de los píxeles resultantes. Si los píxeles resultantes se van a escribir en un búfer de índice de color, o si se vuelven a leer en la memoria del cliente en \_ el formato de índice de color de GL \_ , los píxeles continúan siendo tratados como índices. Si \_ \_ el color del mapa de contabilidad es true, cada índice se enmascara en 2 ^ *n* 1, donde *n* es \_ \_ el mapa de píxeles de contabilidad \_ i \_ a \_ i de \_ tamaño y, a continuación, se sustituye por el contenido del mapa de píxeles de contabilidad \_ \_ \_ i al que \_ \_ indexa el valor enmascarado. El \_ color del mapa GL \_ se especifica con **glPixelTransfer**. El contenido de la asignación de índice se especifica con **glPixelMap**.<br/> Si los píxeles resultantes se van a escribir en un búfer de color RGBA, o si se van a volver a leer en la memoria del cliente con un formato distinto del índice de color de GL \_ \_ , los píxeles se convierten de los índices a los colores mediante la referencia a la asignación de píxeles de contabilidad de cuatro mapas i a \_ \_ \_ \_ \_ R, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ el mapa de píxeles de GL i a la. Antes de desreferenciarse, el índice está enmascarado por 2 n 1, donde n es el \_ mapa de píxeles de GL \_ \_ i \_ a \_ \_ tamaño de R para el mapa rojo, el mapa de píxeles de GL \_ \_ \_ i \_ a \_ G de tamaño para el mapa verde, el tamaño de la asignación de píxeles de \_ GL \_ \_ \_ i \_ a \_ B \_ para el mapa azul y el mapa de píxeles de contabilidad \_ \_ \_ i \_ en \_ un \_ tamaño para el Todos los componentes tomados de las asignaciones se fijan en el intervalo \[ 0, 1 \] . El contenido de las cuatro asignaciones se especifica con **glPixelMap**.<br/> |
| Profundidad       | Cada valor de profundidad se multiplica por \_ escala de profundidad de contabilidad \_ , se agrega a la diferencia de profundidad de contabilidad general \_ \_ y, a continuación, se fija en el intervalo de \[ 0 a 1 \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Cada índice está desplazado por los bits del cambio de índice de contabilidad \_ \_ , al igual que un índice de color, y después se agrega al desplazamiento de índice de contabilidad \_ \_ . Si la \_ \_ Galería de símbolos GL MAP es true, cada índice se enmascara por 2N 1, donde *n* es el \_ \_ tamaño de la asignación \_ de píxeles de GL \_ a \_ s y, \_ a continuación, se reemplaza por el contenido de los mapas de píxeles de GL \_ \_ \_ \_ a \_ s indizados por el valor enmascarado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La función [**glPixelTransferf**](glpixeltransfer.md) se puede usar para establecer cualquier parámetro de transferencia de píxeles. Si el tipo de parámetro es booleano, 0,0 implica false y cualquier otro valor implica true. Si *PName* es un parámetro entero, *param* se redondea al entero más próximo.

Del mismo modo, **glPixelTransferi** también se puede usar para establecer cualquiera de los parámetros de transferencia de píxeles. Los parámetros booleanos se establecen en false si *param* es 0 y true en caso contrario. El parámetro *param* se convierte en el punto flotante antes de asignarse a parámetros con valores reales.

Si un comando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)o [**glTexImage2D**](glteximage2d.md) se coloca en una lista de visualización (vea [**glNewList**](glnewlist.md) y [**glCallList**](glcalllist.md)), la configuración del modo de transferencia de píxeles en vigor cuando se *ejecuta* la lista de visualización son las que se usan. Pueden ser diferentes de los valores cuando el comando se compiló en la lista de visualización.

Las siguientes funciones recuperan información relacionada con **glPixelTransfer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ color de mapa GL \_

**glGet** con el argumento de \_ Galería de símbolos de libro de contabilidad \_

**glGet** con el argumento \_ cambio de índice GL \_

**glGet** con el argumento \_ desplazamiento del índice GL \_

**glGet** con el argumento \_ escala roja de contabilidad \_

**glGet** con el argumento de \_ inclinación rojo de GL \_

**glGet** con el argumento \_ escala verde de contabilidad \_

**glGet** con el argumento de la \_ desviación verde GL \_

**glGet** con el argumento \_ escala azul de contabilidad \_

**glGet** con el argumento de la \_ desviación azul de contabilidad \_

**glGet** con el argumento \_ escala alfa alfa \_

**glGet** con el argumento de la \_ diferencia alfa de GL \_

**glGet** con el argumento \_ escala de profundidad de GL \_

**glGet** con la \_ diferencia de profundidad de contabilidad de los argumentos \_

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

 

 





