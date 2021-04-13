---
title: función glPushClientAttrib (GL. h)
description: Las funciones glPushClientAttrib y glPopClientAttrib guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente. | función glPushClientAttrib (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362355"
---
# <a name="glpushclientattrib-function"></a>glPushClientAttrib función)

Las funciones **glPushClientAttrib** y [**glPopClientAttrib**](glpopclientattrib.md) guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Máscara que indica los atributos que se van a guardar. A continuación se indican las constantes de máscara simbólica y sus Estados de cliente de OpenGL asociados.



| Value                                                                                                                                                                                                                                            | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**\_bit de \_ almacén de píxeles de cliente de contabilidad \_ \_**</dt> </dl>                                             | Atributos de modo de almacenamiento en píxeles.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**\_bit de \_ matriz de vértices de cliente de \_ Contabilidad \_**</dt> </dl>                                          | Atributos de la matriz de vértices.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**\_ \_ Todos los \_ bits attrib \_ de cliente de contabilidad**</dt> </dl> | todos los atributos de estado de cliente que se van a apilar.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**desbordamiento de la pila de GL \_ \_**</dt> </dl> | Se llamó a la función mientras la pila de atributos de cliente estaba llena.<br/> |



## <a name="remarks"></a>Observaciones

La función **glPushClientAttrib** usa su parámetro Mask para determinar qué grupos de variables de estado de cliente se guardan en la pila de atributo de cliente. Puede usar el operador OR bit a bit para unir constantes simbólicas aceptadas para establecer bits y construir una máscara.

La función [**glPopClientAttrib**](glpopclientattrib.md) restaura los valores de las variables de estado de cliente que se guardaron por última vez con **glPushclientAttrib**. Las variables de estado de cliente que no se guardaron previamente permanecen sin cambios. Si se insertan atributos en una pila completa de atributos de cliente o se extraen atributos de una pila vacía, se establece una marca de error y no se realiza ningún otro cambio en el estado de OpenGL. De forma predeterminada, la pila de atributos de cliente está vacía.

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

 

 





