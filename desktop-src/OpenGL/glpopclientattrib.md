---
title: Función glPopClientAttrib (Gl.h)
description: Las funciones glPushClientAttrib y glPopClientAttrib guarda y restaura grupos de variables de estado de cliente en la pila client-attribute. | Función glPopClientAttrib (Gl.h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- Función glPopClientAttrib OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171381"
---
# <a name="glpopclientattrib-function"></a>Función glPopClientAttrib

Las [**funciones glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib** guarda y restaura grupos de variables de estado de cliente en la pila client-attribute.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl> | Se llamó a la función mientras la pila de atributo de cliente estaba llena.<br/> |



## <a name="remarks"></a>Observaciones

La **función glPushClientAttrib** usa su parámetro mask para determinar qué grupos de variables de estado de cliente se guardan en la pila de atributo de cliente. Puede usar el operador OR bit a bit para unir constantes simbólicas aceptadas para establecer bits y construir una máscara.

La **función glPopClientAttrib** restaura los valores de las variables de estado de cliente guardadas por última vez **con glPushclientAttrib**. Las variables de estado de cliente que no se guardaron anteriormente se mantienen sin cambios. Al insertar atributos en una pila de atributos de cliente completa o sacar atributos de una pila vacía, se establece una marca de error y no se realiza ningún otro cambio en el estado OpenGL. De forma predeterminada, la pila de atributos de cliente está vacía.

Algunos valores de estado de cliente openGL no se pueden guardar en la pila de atributo de cliente. Por ejemplo, no puede guardar los estados select o feedback en la pila client-attribute. La profundidad de la pila de atributo de cliente es al menos 16.

Las **funciones glPushclientAttrib** y **glPopClientAttrib** no se compilan en listas de visualización, pero se ejecutan inmediatamente.

Las **funciones glPushClientAttrib** y **glPopClientAttrib** solo pueden insertar y sacar los modos de almacenamiento de píxeles y los estados de cliente de la matriz de vértices. Debe usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib para**](glpopattrib.md) insertar y mostrar los estados que se mantienen en el servidor.

> [!Note]  
> Las **funciones glPushClientAttrib** y **glPopClientAttrib** solo están disponibles en OpenGL versión 1.1 o posterior.

 

Las funciones siguientes recuperan información relacionada **con glPushClientAttrib** **y glPopClientAttrib**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CLIENT \_ ATTRIB STACK \_ \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX CLIENT \_ \_ ATTRIB STACK \_ \_ DEPTH

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

 

 





