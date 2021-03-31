---
title: función glColorMask (GL. h)
description: La función glColorMask habilita y deshabilita la escritura de componentes de color de búfer de fotogramas.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask (función) OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905096"
---
# <a name="glcolormask-function"></a>glColorMask función)

La función **glColorMask** habilita y deshabilita la escritura de componentes de color de búfer de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*alerta* 
</dt> <dd>

Especifique si el rojo puede o no se puede escribir en el fotogramas. Los valores predeterminados son GL \_ true, lo que indica que se puede escribir el componente de color.

</dd> <dt>

*verde* 
</dt> <dd>

Especifique si el color verde puede o no se puede escribir en el fotogramas. El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.

</dd> <dt>

*azul* 
</dt> <dd>

Especifique si el azul puede o no se puede escribir en el fotogramas. El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.

</dd> <dt>

*alpha* 
</dt> <dd>

Especifique si alfa puede o no se puede escribir en fotogramas. El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glColorMask** especifica si los componentes de color individuales de fotogramas se pueden o no se pueden escribir. Por ejemplo, si el valor de *rojo* es GL \_ false, no se realiza ningún cambio en el componente rojo de ningún píxel de ninguno de los búferes de color, independientemente de la operación de dibujo que se intente.

No se pueden controlar los cambios en los distintos bits de los componentes. En su lugar, los cambios se habilitan o deshabilitan para los componentes de color completos.

Las siguientes funciones recuperan información relacionada con **glColorMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ color \_ WRITEMASK

**glGet** con el argumento del \_ modo RGBA de GL \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





