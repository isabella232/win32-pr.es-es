---
title: función gluBuild1DMipmaps (GLU. h)
description: La función gluBuild1DMipmaps crea mapas de bits 1D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps (función) OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676690"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps función)

La función **gluBuild1DMipmaps** crea mapas de bits 1D.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino. Debe ser la \_ textura de GL \_ 1D.

</dd> <dt>

*components* 
</dt> <dd>

El número de componentes de color de la textura. Debe ser 1, 2, 3 o 4.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Los valores siguientes son válidos: GL \_ color \_ index, GL \_ rojo, GL \_ Green, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, \_ luminancia de GL o luminancia de contabilidad general \_ \_ .

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos para los *datos*. Los valores siguientes son válidos: libro de \_ \_ bytes sin signo de GL, \_ bytes de contabilidad, mapa de bits de GL \_ , libro de contabilidad \_ inferior sin signo corto \_ , GL \_ Short, contabilidad de \_ tipo int sin signo, \_ GL \_ int o GL \_ flotante.

</dd> <dt>

*data* 
</dt> <dd>

Puntero a los datos de la imagen en memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluBuild1DMipmaps** obtiene la imagen de entrada y genera todas las imágenes de mipmap (mediante [**gluScaleImage**](gluscaleimage.md)) para que la imagen de entrada se pueda usar como imagen de textura de mipmapped. A continuación, se llama a la función [**glTexImage1D**](glteximage1d.md) para cargar cada una de las imágenes. Si el ancho de la imagen de entrada no es una potencia de dos, la imagen se escala a la potencia más cercana de dos antes de que se generen los mapas MIP.

Un valor devuelto de cero indica que se ha realizado correctamente. De lo contrario, se devuelve un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).

Para obtener una descripción de los valores aceptables para el parámetro *Format* , vea **glTexImage1D**. Para obtener una descripción de los valores aceptables para el parámetro de *tipo* , vea [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





