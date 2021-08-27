---
title: Función glColorMask (Gl.h)
description: La función glColorMask habilita y deshabilita la escritura de componentes de color del búfer de fotogramas.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- Función glColorMask OpenGL
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
ms.openlocfilehash: 1e8b3e9e00eaa294f77813f8e994358cbb473fc4e5c02fce8e5115dc517cae20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081725"
---
# <a name="glcolormask-function"></a>Función glColorMask

La **función glColorMask** habilita y deshabilita la escritura de componentes de color del búfer de fotogramas.

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

*Rojo* 
</dt> <dd>

Especifique si el color rojo puede o no escribirse en el búfer de fotogramas. Los valores predeterminados son GL TRUE, lo que indica que se puede escribir \_ el componente de color.

</dd> <dt>

*Verde* 
</dt> <dd>

Especifique si el verde puede o no escribirse en el búfer de fotogramas. El valor predeterminado es GL \_ TRUE, lo que indica que se puede escribir el componente de color.

</dd> <dt>

*Azul* 
</dt> <dd>

Especifique si el azul se puede escribir o no en el búfer de fotogramas. El valor predeterminado es GL \_ TRUE, lo que indica que se puede escribir el componente de color.

</dd> <dt>

*alpha* 
</dt> <dd>

Especifique si alfa puede o no escribirse en el búfer de fotogramas. El valor predeterminado es GL \_ TRUE, lo que indica que se puede escribir el componente de color.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glColorMask** especifica si los componentes de color individuales del búfer de fotogramas se pueden escribir o no. Si *el color* rojo es GL FALSE, por ejemplo, no se realiza ningún cambio en el componente rojo de ningún píxel en ninguno de los búferes de color, independientemente de la operación de dibujo que se haya \_ intentado.

No se pueden controlar los cambios en los bits individuales de los componentes. En su lugar, los cambios se habilitan o deshabilitan para componentes de color completos.

Las funciones siguientes recuperan información relacionada **con glColorMask**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ COLOR \_ WRITEMASK

**glGet con** el argumento GL \_ RGBA \_ MODE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





