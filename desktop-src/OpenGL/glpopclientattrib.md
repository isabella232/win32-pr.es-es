---
title: función glPopClientAttrib (GL. h)
description: Las funciones glPushClientAttrib y glPopClientAttrib guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente. | función glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glPopClientAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362269"
---
# <a name="glpopclientattrib-function"></a>glPopClientAttrib función)

Las funciones [**glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib** guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**desbordamiento de la pila de GL \_ \_**</dt> </dl> | Se llamó a la función mientras la pila de atributos de cliente estaba llena.<br/> |



## <a name="remarks"></a>Observaciones

La función **glPushClientAttrib** usa su parámetro Mask para determinar qué grupos de variables de estado de cliente se guardan en la pila de atributo de cliente. Puede usar el operador OR bit a bit para unir constantes simbólicas aceptadas para establecer bits y construir una máscara.

La función **glPopClientAttrib** restaura los valores de las variables de estado de cliente que se guardaron por última vez con **glPushclientAttrib**. Las variables de estado de cliente que no se guardaron previamente permanecen sin cambios. Si se insertan atributos en una pila completa de atributos de cliente o se extraen atributos de una pila vacía, se establece una marca de error y no se realiza ningún otro cambio en el estado de OpenGL. De forma predeterminada, la pila de atributos de cliente está vacía.

Algunos valores de estado de cliente de OpenGL no se pueden guardar en la pila de atributo de cliente. Por ejemplo, no puede guardar los Estados SELECT o feedback en la pila Client-Attribute. La profundidad de la pila de atributo de cliente es al menos 16.

Las funciones **glPushclientAttrib** y **glPopClientAttrib** no se compilan en listas de visualización, pero se ejecutan inmediatamente.

Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo pueden mostrar los modos de almacenamiento en píxeles y los Estados de cliente de matriz de vértices. Debe usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para los Estados de envío y de extracción que se mantienen en el servidor.

> [!Note]  
> Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo están disponibles en la versión 1,1 o posterior de OpenGL.

 

Las siguientes funciones recuperan información relacionada con **glPushClientAttrib** y **glPopClientAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumentos \_ profundidad de \_ pila de ATRIB de cliente de \_ Contabilidad \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ Max \_ Client la \_ \_ \_ profundidad de la pila

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





