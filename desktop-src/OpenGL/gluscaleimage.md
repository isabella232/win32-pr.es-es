---
title: función gluScaleImage (GLU. h)
description: La función gluScaleImage escala una imagen a un tamaño arbitrario.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage (función) OpenGL
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
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421902"
---
# <a name="gluscaleimage-function"></a>gluScaleImage función)

La función **gluScaleImage** escala una imagen a un tamaño arbitrario.

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

Formato de los datos de píxeles. Los valores simbólicos siguientes son válidos: el \_ Índice de color \_ de GL, el \_ Índice de la galería de símbolos GL \_ , el \_ componente de profundidad de contabilidad \_ , GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ , GL BGRA ext, GL de \_ \_ Contabilidad y la luminancia de \_ GL \_ \_ .

</dd> <dt>

*ancho* 
</dt> <dd>

Ancho de la imagen de origen que se escala.

</dd> <dt>

*alto* 
</dt> <dd>

Alto de la imagen de origen que se escala.

</dd> <dt>

*escribir* 
</dt> <dd>

El tipo de datos para los *datos*. Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.

</dd> <dt>

*datos* 
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

El tipo de datos para *dataout*. Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.

</dd> <dt>

*dataout* 
</dt> <dd>

Puntero a la imagen de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es cero.

Si se produce un error en la función, el valor devuelto es un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Observaciones

La función **gluScaleImage** escala una imagen de píxeles usando los modos de almacén de píxeles adecuados para desempaquetar los datos de la imagen de origen y empaquetar los datos en la imagen de destino.

Al reducir una imagen, **gluScaleImage** usa un filtro de cuadro para muestrear la imagen de origen y crear píxeles para la imagen de destino. Al aumentar una imagen, los píxeles de la imagen de origen se interpolan linealmente para crear la imagen de destino.

Para obtener una descripción de los valores aceptables para los parámetros *Format*, *typeof* y *typeout* , consulte [**glReadPixels**](glreadpixels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





