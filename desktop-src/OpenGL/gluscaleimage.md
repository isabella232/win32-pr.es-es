---
title: Función gluScaleImage (Glu.h)
description: La función gluScaleImage escala una imagen a un tamaño arbitrario.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- Función gluScaleImage OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a6bab8865dec475087743f658429fd633fc9bb1443da14bd1198e8a7c73b0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488745"
---
# <a name="gluscaleimage-function"></a>función gluScaleImage

La **función gluScaleImage** escala una imagen a un tamaño arbitrario.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Los siguientes valores simbólicos son válidos: GL \_ COLOR \_ INDEX, GL \_ STENCIL \_ INDEX, GL \_ DEPTH \_ \_ COMPONENT, GL RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE y GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*widthin* 
</dt> <dd>

Ancho de la imagen de origen que se escala.

</dd> <dt>

*heightin* 
</dt> <dd>

Alto de la imagen de origen que se escala.

</dd> <dt>

*typein* 
</dt> <dd>

Tipo de datos para *datain*. Debe ser uno de los siguientes: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL INT o \_ GL \_ FLOAT.

</dd> <dt>

*datain* 
</dt> <dd>

Puntero a la imagen de origen.

</dd> <dt>

*widthout* 
</dt> <dd>

Ancho de la imagen de destino.

</dd> <dt>

*heightout* 
</dt> <dd>

Alto de la imagen de destino.

</dd> <dt>

*typeout* 
</dt> <dd>

Tipo de datos para *dataout*. Debe ser uno de los siguientes: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL INT o \_ GL \_ FLOAT.

</dd> <dt>

*salida de datos* 
</dt> <dd>

Puntero a la imagen de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es cero.

Si se produce un error en la función, el valor devuelto es un código de error glu [**(vea gluErrorString).**](gluerrorstring.md)

## <a name="remarks"></a>Comentarios

La **función gluScaleImage** escala una imagen de píxel mediante los modos de almacén de píxeles adecuados para desempaquetar datos de la imagen de origen y empaquetar los datos en la imagen de destino.

Al reducir una imagen, **gluScaleImage** usa un filtro de cuadro para muestrear la imagen de origen y crear píxeles para la imagen de destino. Al ampliar una imagen, los píxeles de la imagen de origen se interpolan linealmente para crear la imagen de destino.

Para obtener una descripción de los valores aceptables para los parámetros *de* formato , *typein* y *typeout,* [**vea glReadPixels**](glreadpixels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





