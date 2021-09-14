---
title: Función glColorPointer (Gl.h)
description: La función glColorPointer define una matriz de colores.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- Función glColorPointer OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362099"
---
# <a name="glcolorpointer-function"></a>Función glColorPointer

La **función glColorPointer** define una matriz de colores.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*size* 
</dt> <dd>

Número de componentes por color. El valor debe ser 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos de cada componente de color de una matriz de colores. Los tipos de datos aceptables se especifican con las siguientes constantes: GL \_ BYTE, \_ GL UNSIGNED \_ BYTE, GL \_ SHORT, GL \_ UNSIGNED \_ SHORT, GL \_ INT, GL \_ UNSIGNED \_ INT, GL \_ FLOAT o GL \_ DOUBLE.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento de bytes entre colores consecutivos. Cuando *stride* es cero, los colores se empaquetan estrechamente en la matriz.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero al primer componente del primer elemento de color de una matriz de colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *el* tamaño no era 3 o 4.<br/>            |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | *Type* no era un valor aceptado.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *stride* o *count era* negativo.<br/> |



## <a name="remarks"></a>Observaciones

La **función glColorPointer** especifica la ubicación y el formato de datos de una matriz de componentes de color que se usará al representar. El *parámetro stride* determina el desplazamiento de bytes de un color al siguiente, lo que habilita el empaquetado de atributos de vértice en una sola matriz o almacenamiento en matrices independientes. En algunas implementaciones, el almacenamiento de atributos de vértice en una sola matriz puede ser más eficaz que el uso de matrices independientes.

Se ha habilitado la matriz de colores especificando la constante GL \_ COLOR \_ ARRAY con [**glEnableClientState**](glenableclientstate.md). Al [**llamar a glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) se usa la matriz de colores que está habilitada. De forma predeterminada, la matriz de colores está deshabilitada. Las **llamadas a glColorPointer** no se pueden especificar en las listas para mostrar.

Cuando se especifica una matriz de colores mediante **glColorPointer**, los valores de todos los parámetros de la matriz de colores de la función se guardan en un estado del lado cliente y se pueden almacenar en caché elementos de matriz estáticos. Dado que los parámetros de la matriz de colores están en estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardarán ni restaurarán los valores de los parámetros.

Aunque la especificación de la matriz de colores dentro de los pares [**glBegin**](glbegin.md) y [**glBegin**](glend.md) no genera un error, los resultados son indefinidos.

Las siguientes funciones recuperan información relacionada con **la función glColorPointer:**

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ COLOR \_ ARRAY

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ COLOR ARRAY \_ \_ SIZE

**glGet con** el argumento GL \_ COLOR ARRAY \_ \_ TYPE

**glGet con** el argumento GL \_ COLOR ARRAY \_ \_ STRIDE

**glGet con** el argumento GL \_ COLOR ARRAY \_ \_ COUNT

[**glGetPointerv con el**](glgetpointerv.md) argumento GL \_ COLOR ARRAY \_ \_ POINTER

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





