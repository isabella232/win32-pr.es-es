---
title: Función gluBuild2DMipmaps (Glu.h)
description: La función gluBuild2DMipmaps crea mapas MIP 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- Función GluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27dcf3d0e95b0b52d5b7f4c4ce0e5692f3fc856b81d9c1d82c9661a70e2f818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489655"
---
# <a name="glubuild2dmipmaps-function"></a>Función gluBuild2DMipmaps

La **función gluBuild2DMipmaps** crea mapas MIP 2D.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino. Debe ser GL \_ TEXTURE \_ 2D.

</dd> <dt>

*components* 
</dt> <dd>

Número de componentes de color de la textura. Debe ser 1, 2, 3 o 4.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la imagen de textura.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxel. Debe ser uno de los siguientes: GL \_ COLOR \_ INDEX, GL \_ RED, \_ GL GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE o GL \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos para *los datos*. Debe ser uno de los siguientes: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT o GL \_ FLOAT.

</dd> <dt>

*data* 
</dt> <dd>

Puntero a los datos de imagen en memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La función **gluBuild2DMipmaps** obtiene la imagen de entrada y genera todas las imágenes de mapa mipmap (mediante [**gluScaleImage),**](gluscaleimage.md)por lo que la imagen de entrada se puede usar como una imagen de textura mipmapped. Para cargar cada una de las imágenes, llame [**a glTexImage2D.**](glteximage2d.md) Si las dimensiones de la imagen de entrada no son potencias de dos, la imagen se escala para que tanto el ancho como el alto sean potencias de dos antes de que se generen los mapas MIP.

Un valor devuelto de cero indica que se ha correcto. De lo contrario, se devuelve un código de error glu [**(vea gluErrorString).**](gluerrorstring.md)

Para obtener una descripción de los valores aceptables para el *parámetro format,* vea **glTexImage2D**. Para obtener una descripción de los valores aceptables para *el tipo*, [**vea glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





