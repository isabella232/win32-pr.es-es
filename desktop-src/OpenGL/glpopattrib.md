---
title: Función glPopAttrib (Gl.h)
description: Abre la pila de atributos.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- Función glPopAttrib OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171385"
---
# <a name="glpopattrib-function"></a>Función glPopAttrib

Abre la pila de atributos.

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
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Se llamó a la función mientras la pila de atributos estaba vacía.<br/>                                                               |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La [**función glPushAttrib**](glpushattrib.md) toma un argumento, una máscara que indica qué grupos de variables de estado se deben guardar en la pila de atributos. Las constantes simbólicas se usan para establecer bits en la máscara. Normalmente, el parámetro mask se construye mediante **or** que une varias de estas constantes. La máscara especial GL \_ ALL \_ ATTRIB \_ BITS se puede usar para guardar todos los estados apilables.

La **función glPopAttrib** restaura los valores de las variables de estado guardadas con el último [**comando glPushAttrib.**](glpushattrib.md) Los no guardados se mantienen sin cambios.

Es un error insertar atributos en una pila completa o quitar atributos de una pila vacía. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado OpenGL.

Inicialmente, la pila de atributos está vacía.

No todos los valores del estado OpenGL se pueden guardar en la pila de atributos. Por ejemplo, el estado de empaquetado y desempaquete de píxeles, el estado del modo de representación y la selección y el estado de comentarios no se pueden guardar.

La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.

Las siguientes funciones recuperan información relacionada [**con glPushAttrib**](glpushattrib.md) y **glPopAttrib**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX \_ ATTRIB STACK \_ \_ DEPTH

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





