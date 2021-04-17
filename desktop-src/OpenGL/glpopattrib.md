---
title: función glPopAttrib (GL. h)
description: Extrae la pila de atributos.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666023"
---
# <a name="glpopattrib-function"></a>glPopAttrib función)

Extrae la pila de atributos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**subdesbordamiento de la pila de GL \_ \_**</dt> </dl>   | Se llamó a la función mientras la pila de atributos estaba vacía.<br/>                                                               |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función [**glPushAttrib**](glpushattrib.md) toma un argumento, una máscara que indica los grupos de variables de estado que se van a guardar en la pila de atributos. Las constantes simbólicas se utilizan para establecer bits en la máscara. Normalmente, el parámetro Mask se construye **mediante la** combinación de varias de estas constantes. La máscara especial GL \_ todos \_ los \_ bits attrib se pueden usar para guardar todos los Estados apilables.

La función **glPopAttrib** restaura los valores de las variables de estado guardadas con el último comando [**glPushAttrib**](glpushattrib.md) . Los que no se han guardado permanecen inalterados.

Es un error insertar atributos en una pila completa o desactivar los atributos de una pila vacía. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.

Inicialmente, la pila de atributos está vacía.

No todos los valores del estado de OpenGL se pueden guardar en la pila de atributos. Por ejemplo, el estado del paquete de píxeles y desempaquetado, el estado del modo de representación y el estado de selección y de comentarios no se pueden guardar.

La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.

Las siguientes funciones recuperan información relacionada con [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ pila de atrib \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ profundidad máxima de la pila de Max \_ \_ \_

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





