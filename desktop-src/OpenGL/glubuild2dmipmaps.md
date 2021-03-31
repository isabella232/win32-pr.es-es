---
title: función gluBuild2DMipmaps (GLU. h)
description: La función gluBuild2DMipmaps crea mapas de bits 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps (función) OpenGL
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
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996093"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps función)

La función **gluBuild2DMipmaps** crea mapas de bits 2D.

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

Textura de destino. Debe ser la \_ textura de GL \_ 2D.

</dd> <dt>

*components* 
</dt> <dd>

El número de componentes de color de la textura. Debe ser 1, 2, 3 o 4.

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

Formato de los datos de píxeles. Debe ser uno de los siguientes: GL \_ color \_ index, GL \_ rojo, GL \_ Green, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, \_ luminancia de GL o luminancia de contabilidad general \_ \_ .

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos para los *datos*. Debe ser uno de los siguientes: \_ bytes sin signo de libro \_ de contabilidad, \_ bytes de contabilidad, mapa de bits de GL \_ , GL \_ sin signo \_ corto, GL \_ Short, libro de contabilidad \_ sin signo \_ \_ \_ de contab.

</dd> <dt>

*data* 
</dt> <dd>

Puntero a los datos de la imagen en memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluBuild2DMipmaps** obtiene la imagen de entrada y genera todas las imágenes de mipmap (mediante [**gluScaleImage**](gluscaleimage.md)), por lo que la imagen de entrada se puede usar como imagen de textura de mipmapped. Para cargar cada una de las imágenes, llame a [**glTexImage2D**](glteximage2d.md). Si las dimensiones de la imagen de entrada no son potencias de dos, la imagen se escala para que el ancho y el alto sean potencias de dos antes de que se generen los mapas MIP.

Un valor devuelto de cero indica que se ha realizado correctamente. De lo contrario, se devuelve un código de error GLU (vea [**gluErrorString**](gluerrorstring.md)).

Para obtener una descripción de los valores aceptables para el parámetro *Format* , vea **glTexImage2D**. Para obtener una descripción de los valores aceptables para el *tipo*, vea [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





