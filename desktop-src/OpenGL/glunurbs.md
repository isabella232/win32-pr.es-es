---
title: Función gluNurbsCallback (Glu.h)
description: La función gluNurbsCallback define una devolución de llamada para un objeto B-Spline racionalizado no uniforme (NUTBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- Función GluNurbsCallback OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169217"
---
# <a name="glunurbscallback-function"></a>función gluNurbsCallback

La **función gluNurbsCallback** define una devolución de llamada para un objeto B-Spline racionalizado no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*Que* 
</dt> <dd>

Devolución de llamada que se está definindo. El único valor válido es GLU \_ ERROR. El significado de GLU ERROR significa que se llama a la función \_ de error cuando se encuentra un error. Su único argumento es de **tipo GLenum** e indica el error específico que se produjo. Hay 37 errores únicos de LABS, denominados GLU \_ GLU GLUBS \_ ERROR1 a TRAVÉS DE \_ GLUBS \_ ERROR37. Las cadenas de caracteres que describen estos errores se pueden recuperar [**con gluErrorString.**](gluerrorstring.md)

</dd> <dt>

*fn* 
</dt> <dd>

Puntero a la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluNurbsCallback para** definir una devolución de llamada que va a usar un objeto RECORDSETBS. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *fn* es **NULL**, se borra cualquier devolución de llamada existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





