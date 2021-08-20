---
title: Función glPixelStoref (Gl.h)
description: Establece los modos de almacenamiento de píxeles. | Función glPixelStoref (Gl.h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- Función glPixelStoref OpenGL
topic_type:
- apiref
api_name:
- glPixelStoref
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928cf7ccc054a94840e146e0e2ce6a7afdb74f7cde5f59569ec1cf71acbb3dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128085"
---
# <a name="glpixelstoref-function"></a>Función glPixelStoref

Establece los modos de almacenamiento de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pname* 
</dt> <dd>

Nombre simbólico del parámetro que se va a establecer. Seis de los parámetros de almacenamiento afectan a cómo se devuelven los datos de píxeles a la memoria del cliente y, por tanto, solo son significativos para [**los comandos glReadPixels.**](glreadpixels.md) Los pasos son los siguientes:



| Storage Parámetro                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BYTES DE \_ INTERCAMBIO \_ DEL PAQUETE \_ GL                                       | Si es true, se invierte el orden de bytes para los componentes de color multibyte, los componentes de profundidad, los índices de color o los índices de galería de símbolos. Es decir, si un componente de cuatro bytes está hecho de bytes *b* 0 , *b* 1 , *b* 2, *b* 3 , se almacena en memoria como *b* 3 , *b* 2, *b* 1, *b* 0 si GL PACK SWAP BYTES \_ es \_ \_ true. GL PACK SWAP BYTES no tiene ningún efecto en el orden de memoria de los componentes dentro de un píxel, solo en el orden de bytes dentro de \_ \_ componentes o \_ índices. Por ejemplo, los tres componentes de un píxel de formato GL RGB siempre se almacenan con el primero rojo, el segundo verde y el tercero azul, independientemente del valor de \_ GL \_ PACK SWAP \_ \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                               |
| GL \_ PACK \_ LSB \_ FIRST                                        | Si es true, los bits se ordenan dentro de un byte de menos significativo a más significativo; de lo contrario, el primer bit de cada byte es el más significativo. Este parámetro es significativo solo para los datos de mapa de bits.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| LONGITUD DE \_ FILA \_ DEL PAQUETE \_ GL                                       | Si es mayor que cero, GL \_ PACK ROW LENGTH define el número de \_ \_ píxeles de una fila. Si el primer píxel de una fila se coloca en la ubicación p en memoria, la ubicación del primer píxel de la fila siguiente se obtiene omitiendo Ecuación que muestra la ubicación del primer píxel de la fila siguiente ![ en GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ Componentes o índices de nueva línea, donde n es el número de componentes o índices de un píxel, l es el número de píxeles de una fila (gl pack row length si es mayor que cero, el argumento de ancho de la rutina de píxeles en caso contrario), un es el valor de gl pack alignment y s es el tamaño, en bytes, de un único componente \]   \- \- \-  \- \- (si    <     =  es , entonces es como si un s ). En el caso de los valores de 1 bit, la ubicación de la fila siguiente se obtiene omitiendo Ecuación que muestra la ubicación de la fila siguiente ![ en GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componentes o índices. El componente *de palabra* de esta descripción hace referencia a los valores que no son de índice rojo, verde, azul, alfa y profundidad. Storage formato GL RGB, por ejemplo, tiene tres componentes por píxel: primero \_ rojo, después verde y finalmente azul.<br/> |
| GL \_ PACK SKIP PIXELS \_ \_ y <br/> GL \_ PACK \_ SKIP \_ ROWS | Estos valores se proporcionan para mayor comodidad para el programador. no proporcionan ninguna funcionalidad que no se pueda duplicar simplemente incrementando el puntero pasado [**a glReadPixels**](glreadpixels.md). Establecer GL PACK SKIP PIXELS en i equivale a incrementar el puntero por i n componentes o índices, donde n es el número de componentes o índices \_ \_ de cada \_ píxel.    Establecer GL PACK SKIP ROWS en j equivale a incrementar el puntero en componentes o índices j k, donde k es el número de componentes o índices por fila, como se calculó anteriormente en la sección \_ \_ GL PACK ROW \_    \_ \_ \_ LENGTH.                                                                                                                                                                                                                                                                                                                                                                                                   |
| ALINEACIÓN \_ DEL PAQUETE \_ GL                                         | Especifica los requisitos de alineación para el inicio de cada fila de píxeles en memoria. Los valores permitidos son 1 (alineación de bytes), 2 (filas alineadas con bytes numerados uniformes), 4 (alineación de palabras) y 8 (las filas comienzan en límites de doble palabra).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Los otros seis parámetros de almacenamiento afectan a cómo se leen los datos de píxeles de la memoria del cliente. Estos valores son significativos para [**glDrawPixels,**](gldrawpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)y [**glPolygonStipple.**](glpolygonstipple.md) Los pasos son los siguientes:



| Storage Parámetro                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ UNPACK \_ SWAP \_ BYTES                                         | Si es true, se invierte el orden de bytes para los componentes de color multibyte, los componentes de profundidad, los índices de color o los índices de galería de símbolos. Es decir, si un componente de cuatro bytes está hecho de bytes *b* 0 , *b* 1 , *b* 2 , *b* 3 , se almacena en memoria como *b* 3, *b* 2, *b* 1, *b* 0 si GL \_ UNPACK SWAP \_ BYTES es \_ true. GL UNPACK SWAP BYTES no tiene ningún efecto en el orden de memoria de los componentes dentro de un píxel, solo en el orden de bytes dentro de \_ \_ componentes o \_ índices. Por ejemplo, los tres componentes de un píxel de formato GL RGB siempre se almacenan con rojo primero, segundo verde y tercero azul, independientemente del valor de \_ GL \_ UNPACK \_ SWAP \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ UNPACK \_ LSB \_ FIRST                                          | Si es true, los bits se ordenan dentro de un byte de menos significativo a más significativo; de lo contrario, el primer bit de cada byte es el más significativo. Esto es significativo solo para los datos de mapa de bits.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GL \_ UNPACK \_ ROW \_ LENGTH                                         | Si es mayor que cero, GL \_ UNPACK \_ ROW LENGTH define el número de \_ píxeles de una fila. Si el primer píxel de una fila se coloca en la ubicación p en memoria, la ubicación del primer píxel de la fila siguiente se obtiene omitiendo Ecuación que muestra la ubicación del primer píxel de la fila siguiente ![ en GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ Componentes o índices de nueva línea, donde n es el número de componentes o índices de un píxel, l es el número de píxeles de una fila (gl pack row length si es mayor que cero, el argumento de ancho de la rutina de píxeles en caso contrario), un es el valor de gl pack alignment y s es el tamaño, en bytes, de un único componente \]   \- \- \-  \- \- (si    <     =  es , entonces es como si un s ). En el caso de los valores de 1 bit, la ubicación de la fila siguiente se obtiene omitiendo Ecuación que muestra la ubicación de la fila siguiente ![ en GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componentes o índices. El componente *de palabra* de esta descripción hace referencia a los valores que no son de índice rojo, verde, azul, alfa y profundidad. Storage formato GL RGB, por ejemplo, tiene tres componentes por píxel: primero \_ rojo, después verde y finalmente azul.<br/> |
| GL \_ UNPACK \_ SKIP PIXELS \_ y <br/> GL \_ UNPACK \_ SKIP \_ ROWS | Estos valores se proporcionan para mayor comodidad para el programador. no proporcionan ninguna funcionalidad que no se pueda duplicar simplemente incrementando el puntero pasado a [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)o [**glPolygonStipple.**](glpolygonstipple.md) Establecer GL UNPACK SKIP PIXELS en i equivale a incrementar el puntero por i n componentes o índices, donde n es el número de componentes o índices \_ \_ de cada \_ píxel.    Establecer GL UNPACK SKIP ROWS en j equivale a incrementar el puntero en componentes o índices j k, donde k es el número de componentes o índices por fila, como se calculó anteriormente en la sección \_ \_ GL \_ UNPACK ROW    \_ \_ \_ LENGTH.                                                                                                                                                                                                                                    |
| ALINEACIÓN \_ DE DESEMPAQUETE \_ DE GL                                           | Especifica los requisitos de alineación para el inicio de cada fila de píxeles en memoria. Los valores permitidos son 1 (alineación de bytes), 2 (filas alineadas con bytes numerados uniformes), 4 (alineación de palabras) y 8 (las filas comienzan en límites de doble palabra).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor en el que se establece *pname.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La función **glPixelStore** establece modos de almacenamiento de píxeles que afectan al funcionamiento de las posteriores [**glDrawPixels**](gldrawpixels.md) y [**glReadPixels,**](glreadpixels.md) así como al desempaquetado de patrones detippla de polígono (vea [**glPolygonStipple),**](glpolygonstipple.md)mapas de bits (vea [**glBitmap)**](glbitmap.md)y patrones de textura (vea [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D).**](gltexsubimage2d.md)

En la tabla siguiente se proporciona el tipo, el valor inicial y el intervalo de valores válidos para cada uno de los parámetros de almacenamiento que se pueden establecer con **glPixelStore**.



| Pname                    | Tipo    | Valor inicial | Intervalo válido   |
|--------------------------|---------|---------------|---------------|
| BYTES DE \_ INTERCAMBIO \_ DEL PAQUETE \_ GL    | Boolean | false         | true o false |
| BYTES DE \_ INTERCAMBIO \_ DEL PAQUETE \_ GL    | Boolean | false         | true o false |
| LONGITUD DE \_ FILA \_ DEL PAQUETE \_ GL    | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ ROWS     | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ PIXELS   | integer | 0             | \[0,?)        |
| ALINEACIÓN \_ DEL PAQUETE \_ GL      | integer | 4             | 1, 2, 4 u 8 |
| GL \_ UNPACK \_ SWAP \_ BYTES  | Boolean | false         | true o false |
| GL \_ UNPACK \_ LSB \_ FIRST   | Boolean | false         | true o false |
| GL \_ UNPACK \_ ROW \_ LENGTH  | integer | 0             | \[0,?)        |
| GL \_ UNPACK \_ SKIP \_ ROWS   | integer | 0             | \[0,?)        |
| GL \_ UNPACK \_ SKIP \_ PIXELS | integer | 0             | \[0,?)        |
| ALINEACIÓN \_ DE DESEMPAQUETE \_ DE GL    | integer | 4             | 1, 2, 4 u 8 |



 

La **función glPixelStoref** se puede usar para establecer cualquier parámetro de almacén de píxeles. Si el tipo de parámetro es booleano y *param* es 0,0, el parámetro es false; de lo contrario, se establece en true. Si *pname* es un parámetro de tipo entero, *param* se redondea al entero más cercano.

Del mismo modo, la **función glPixelStorei** también se puede usar para establecer cualquiera de los parámetros de almacén de píxeles. Los parámetros booleanos se establecen en false si *param* es 0 y true en caso contrario. El *parámetro param* se convierte en punto flotante antes de asignarse a parámetros con valores reales.

Los modos de almacenamiento de píxeles en vigor cuando [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md) se colocan en un control de lista de visualización la interpretación de los datos de memoria. Los modos de almacenamiento de píxeles en vigor cuando se ejecuta una lista de visualización no son significativos.

Las siguientes funciones recuperan información relacionada **con glPixelStore**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ PACK SWAP \_ \_ BYTES

**glGet** con el argumento GL \_ PACK \_ LSB \_ FIRST

**glGet con** el argumento GL \_ PACK ROW \_ \_ LENGTH

**glGet con** el argumento GL \_ PACK SKIP \_ \_ ROWS

**glGet con** el argumento GL \_ PACK SKIP \_ \_ PIXELS

**glGet con** el argumento GL \_ PACK \_ ALIGNMENT

**glGet con** el argumento GL \_ UNPACK \_ SWAP \_ BYTES

**glGet** con el argumento GL \_ UNPACK \_ LSB \_ FIRST

**glGet con** el argumento GL \_ UNPACK \_ ROW \_ LENGTH

**glGet con** el argumento GL \_ UNPACK \_ SKIP \_ ROWS

**glGet con** el argumento GL \_ UNPACK \_ SKIP \_ PIXELS

**glGet** con el argumento GL \_ UNPACK \_ ALIGNMENT

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





