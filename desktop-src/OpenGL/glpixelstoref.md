---
title: función glPixelStoref (GL. h)
description: Establece modos de almacenamiento en píxeles. | función glPixelStoref (GL. h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- glPixelStoref (función) OpenGL
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
ms.openlocfilehash: dc35613be68bb142b14a7e8278d6e0b89f05d78e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104550010"
---
# <a name="glpixelstoref-function"></a>glPixelStoref función)

Establece modos de almacenamiento en píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PName* 
</dt> <dd>

Nombre simbólico del parámetro que se va a establecer. Seis de los parámetros de almacenamiento afectan a cómo se devuelven los datos de píxeles a la memoria del cliente y, por lo tanto, son significativos solo para los comandos [**glReadPixels**](glreadpixels.md) . Los pasos son los siguientes:



| Parámetro Storage                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ bytes de intercambio de paquete de contabilidad \_                                       | Si es true, se invierte el orden de los bytes para componentes de color multibyte, componentes de profundidad, índices de color o índices de estarcido. Es decir, si un componente de cuatro bytes se compone de bytes *b* 0, *b* 1, *b 2*, *b* 3, se almacena en la memoria como *b* 3, *b* 2, *b* 1, *b* 0 si los \_ bytes de intercambio del paquete GL \_ \_ son true. Los \_ \_ \_ bytes de intercambio de paquetes de contabilidad no afectan al orden de la memoria de los componentes de un píxel, solo en el orden de los bytes dentro de los componentes o índices. Por ejemplo, los tres componentes de un píxel con formato de libro de contabilidad \_ RGB siempre se almacenan con el color rojo primero, el segundo verde y el tercero azul, independientemente del valor de \_ \_ bytes de intercambio de paquete de contabilidad \_ .                                                                                                                                                                                                                                                                                                                                                                                               |
| \_primer paquete de GL \_ LSB \_                                        | Si es true, los bits se ordenan en un byte de menos significativo a más significativo; de lo contrario, el primer bit de cada byte es el más significativo. Este parámetro solo es importante para los datos de mapa de bits.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_longitud de \_ fila del paquete de contabilidad \_                                       | Si es mayor que cero, \_ \_ \_ la longitud de fila del paquete de contabilidad define el número de píxeles de una fila. Si el primer píxel de una fila se coloca en la ubicación p en la memoria, se obtiene la ubicación del primer píxel de la siguiente fila omitiendo ![ la ecuación que muestra la ubicación del primer píxel de la fila siguiente en GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ \]los componentes o índices de nueva línea, donde *n* es el número de componentes o índices de un píxel. *l* es el número de píxeles de una fila ( \- la longitud de la fila del paquete GL \- \- si es mayor que cero, el argumento de ancho de la rutina de píxeles en caso contrario), *a* es el valor de la alineación del \- paquete GL \- y *s* es el tamaño, en bytes, de un componente único (si   <  es, entonces es como si a   =  ). en el caso de valores de 1 bit, se obtiene la ubicación de la siguiente fila omitiendo la ![ ecuación que muestra la ubicación de la siguiente fila en GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componentes o índices. El *componente* de Word de esta descripción hace referencia a los valores de no índice rojo, verde, azul, alfa y profundidad. El formato de almacenamiento GL \_ RGB, por ejemplo, tiene tres componentes por píxel: primer rojo, verde y azul.<br/> |
| Paquete de libro de contabilidad \_ \_ omitir \_ píxeles y <br/> paquete de libro de contabilidad; \_ \_ omitir \_ filas | Estos valores se proporcionan por comodidad al programador; no proporcionan ninguna funcionalidad que no se pueda duplicar con solo incrementar el puntero que se pasa a [**glReadPixels**](glreadpixels.md). La configuración del paquete de libro \_ \_ de contabilidad omite \_ los píxeles en *i* es equivalente a incrementar el puntero por *i n* componentes o índices, donde *n* es el número de componentes o índices de cada píxel. La configuración \_ del paquete de libro \_ de contabilidad omite \_ las filas en *j* equivale a incrementar el puntero con los componentes o índices de *j k* , donde *k* es el número de componentes o índices por fila, tal como se ha calculado anteriormente en la sección de longitud de fila de paquete de contabilidad \_ \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_alineación del paquete GL \_                                         | Especifica los requisitos de alineación para el inicio de cada fila de píxeles en memoria. Los valores permitidos son 1 (alineación de bytes), 2 (filas alineadas con bytes de números pares), 4 (alineación de palabras) y 8 (las filas se inician en límites de palabras dobles).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Los otros seis parámetros de almacenamiento afectan a cómo se leen los datos de píxeles de la memoria del cliente. Estos valores son significativos para [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)y [**glPolygonStipple**](glpolygonstipple.md). Los pasos son los siguientes:



| Parámetro Storage                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ bytes de intercambio de desempaquetado de contabilidad \_                                         | Si es true, se invierte el orden de los bytes para componentes de color multibyte, componentes de profundidad, índices de color o índices de estarcido. Es decir, si un componente de cuatro bytes se compone de bytes *b* 0, *b* 1, *b 2*, *b* 3, se almacena en la memoria como *b* 3, *b* 2, *b* 1, *b* 0 si los \_ bytes de intercambio de desempaquetado de contabilidad \_ \_ son verdaderos. Los \_ \_ \_ bytes de intercambio de desempaquetado de contabilidad no tienen ningún efecto en el orden de la memoria de los componentes de un píxel, solo en el orden de los bytes dentro de los componentes o índices. Por ejemplo, los tres componentes de un \_ píxel con formato RGB de GL siempre se almacenan con el rojo primero, el segundo verde y el tercero azul, independientemente del valor de \_ bytes de intercambio de desempaquetado de contabilidad \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                           |
| LSB de libro de contabilidad \_ desempaquetado \_ \_ primero                                          | Si es true, los bits se ordenan en un byte de menos significativo a más significativo; de lo contrario, el primer bit de cada byte es el más significativo. Esto solo es importante para los datos de mapa de bits.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_longitud de fila del DESempaquetado de contabilidad \_ \_                                         | Si es mayor que cero, \_ \_ la longitud de fila de desempaquetar libro \_ de contabilidad define el número de píxeles de una fila. Si el primer píxel de una fila se coloca en la ubicación p en la memoria, se obtiene la ubicación del primer píxel de la siguiente fila omitiendo ![ la ecuación que muestra la ubicación del primer píxel de la fila siguiente en GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ \]los componentes o índices de nueva línea, donde *n* es el número de componentes o índices de un píxel. *l* es el número de píxeles de una fila ( \- la longitud de la fila del paquete GL \- \- si es mayor que cero, el argumento de ancho de la rutina de píxeles en caso contrario), *a* es el valor de la alineación del \- paquete GL \- y *s* es el tamaño, en bytes, de un componente único (si   <  es, entonces es como si a   =  ). en el caso de valores de 1 bit, se obtiene la ubicación de la siguiente fila omitiendo la ![ ecuación que muestra la ubicación de la siguiente fila en GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componentes o índices. El *componente* de Word de esta descripción hace referencia a los valores de no índice rojo, verde, azul, alfa y profundidad. El formato de almacenamiento GL \_ RGB, por ejemplo, tiene tres componentes por píxel: primer rojo, verde y azul.<br/> |
| \_DESempaquetar libro \_ de contabilidad omitir \_ píxeles y <br/> desempaquetar libro de contabilidad \_ \_ omitir \_ filas | Estos valores se proporcionan por comodidad al programador; no proporcionan ninguna funcionalidad que no se pueda duplicar con solo incrementar el puntero que se pasa a [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md). Configurar \_ el DESempaquetado de contabilidad \_ omitir \_ píxeles en *i* es equivalente a incrementar el puntero por *i n* componentes o índices, donde *n* es el número de componentes o índices de cada píxel. La configuración de \_ DESempaquetar libro \_ de contabilidad omitir \_ filas en *j* es equivalente a incrementar el puntero con los componentes o índices de *j k* , donde *k* es el número de componentes o índices por fila, tal y como se calculó anteriormente en la sección de la \_ longitud de fila desempaquetar libro de contabilidad \_ \_ .                                                                                                                                                                                                                                    |
| \_alineación del DESempaquetado de contabilidad \_                                           | Especifica los requisitos de alineación para el inicio de cada fila de píxeles en memoria. Los valores permitidos son 1 (alineación de bytes), 2 (filas alineadas con bytes de números pares), 4 (alineación de palabras) y 8 (las filas se inician en límites de palabras dobles).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor que *PName* está establecido en.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glPixelStore** establece los modos de almacenamiento en píxeles que afectan al funcionamiento de los [**glDrawPixels**](gldrawpixels.md) y [**glReadPixels**](glreadpixels.md) posteriores, así como al desempaquetamiento de los patrones de polígono punteado (vea [**glPolygonStipple**](glpolygonstipple.md)), mapas de bits (vea [**glBitmap**](glbitmap.md)) y patrones de textura (vea [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)y [**glTexSubImage2D**](gltexsubimage2d.md)).

En la tabla siguiente se proporciona el tipo, el valor inicial y el intervalo de valores válidos para cada uno de los parámetros de almacenamiento que se pueden establecer con **glPixelStore**.



| PName                    | Tipo    | Valor inicial | Intervalo válido   |
|--------------------------|---------|---------------|---------------|
| \_ \_ bytes de intercambio de paquete de contabilidad \_    | Boolean | false         | true o false |
| \_ \_ bytes de intercambio de paquete de contabilidad \_    | Boolean | false         | true o false |
| \_longitud de \_ fila del paquete de contabilidad \_    | integer | 0             | \[0,?)        |
| paquete de libro de contabilidad; \_ \_ omitir \_ filas     | integer | 0             | \[0,?)        |
| el \_ paquete de contabilidad \_ omite los \_ píxeles   | integer | 0             | \[0,?)        |
| \_alineación del paquete GL \_      | integer | 4             | 1, 2, 4 u 8 |
| \_ \_ bytes de intercambio de desempaquetado de contabilidad \_  | Boolean | false         | true o false |
| LSB de libro de contabilidad \_ desempaquetado \_ \_ primero   | Boolean | false         | true o false |
| \_longitud de fila del DESempaquetado de contabilidad \_ \_  | integer | 0             | \[0,?)        |
| desempaquetar libro de contabilidad \_ \_ omitir \_ filas   | integer | 0             | \[0,?)        |
| desempaquetar libro de contabilidad \_ \_ omitir \_ píxeles | integer | 0             | \[0,?)        |
| \_alineación del DESempaquetado de contabilidad \_    | integer | 4             | 1, 2, 4 u 8 |



 

La función **glPixelStoref** se puede usar para establecer cualquier parámetro de almacén de píxeles. Si el tipo de parámetro es booleano, y si *param* es 0,0, el parámetro es false. en caso contrario, se establece en true. Si *PName* es un parámetro de tipo entero, *param* se redondea al entero más próximo.

Del mismo modo, la función **glPixelStorei** también se puede usar para establecer cualquiera de los parámetros de almacén de píxeles. Los parámetros booleanos se establecen en false si *param* es 0 y true en caso contrario. El parámetro *param* se convierte en el punto flotante antes de asignarse a parámetros con valores reales.

Los modos de almacenamiento en píxeles en vigor cuando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)o [**glPolygonStipple**](glpolygonstipple.md) se colocan en una lista de visualización controlan la interpretación de los datos de memoria. Los modos de almacenamiento en píxeles en vigor cuando se ejecuta una lista de visualización no son significativos.

Las siguientes funciones recuperan información relacionada con **glPixelStore**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumentos de \_ intercambio de paquete de libro de contabilidad \_ \_

**glGet** con el argumento GL \_ Pack \_ LSB \_ primero

**glGet** con argumento de \_ \_ longitud de fila de paquete de contabilidad \_

**glGet** con el argumento paquete de libro de contabilidad \_ \_ omitir \_ filas

**glGet** con argumentos del paquete de libro de contabilidad \_ \_ omitir \_ píxeles

**glGet** con el argumento \_ alineación del paquete GL \_

**glGet** con argumento en el que se \_ desempaquetan los \_ \_ BYTEs de intercambio de contabilidad

**glGet** con el argumento GL \_ desempaquetar \_ LSB \_ primero

**glGet** con argumento de la \_ longitud de fila DESempaquetar libro \_ \_

**glGet** con el argumento GL \_ desempaquetar \_ \_ filas SKIP

**glGet** con el argumento libro de contabilidad \_ desempaquetado \_ omitir \_ píxeles

**glGet** con el argumento \_ alineación desempaquetar libro de contabilidad \_

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

 

 





