---
title: Función glPolygonOffset (Gl.h)
description: La función glPolygonOffset establece la escala y las unidades que Usa OpenGL para calcular los valores de profundidad.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- Función glPolygonOffset OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314372c0ce87ef5b75db24e4482d6b621422546abe0c71a34cc9821cb4391997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614921"
---
# <a name="glpolygonoffset-function"></a>función glPolygonOffset

La **función glPolygonOffset establece** la escala y las unidades que Usa OpenGL para calcular los valores de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Factor* 
</dt> <dd>

Especifica un factor de escala que se usa para crear un desplazamiento de profundidad variable para cada polígono. El valor inicial es cero.

</dd> <dt>

*Unidades* 
</dt> <dd>

Especifica un valor multiplicado por un valor específico de la implementación para crear un desplazamiento de profundidad constante. El valor inicial es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Cuando se habilita GL POLYGON OFFSET, el valor de profundidad de cada fragmento se desplazará después de interpolarse a partir de los valores de profundidad de \_ \_ los vértices adecuados. El valor del desplazamiento es *el factor* ?z + unidades de r , donde ?z es una medida del cambio en profundidad con respecto al área de pantalla del polígono, y r es el valor más pequeño que se garantiza que genera un desplazamiento resolvible para una \* \* implementación determinada. El desplazamiento se agrega antes de que se realice la prueba de profundidad y antes de que el valor se escriba en el búfer de profundidad.

La **función glPolygonOffset** es útil para representar imágenes de línea oculta, para aplicar lascales a las superficies y para representar sólidos con bordes resaltados.

La **función glPolygonOffset** no tiene ningún efecto en las coordenadas de profundidad colocadas en el búfer de comentarios. Tampoco tiene ningún efecto en la selección.

Las siguientes funciones recuperan información relacionada **con glPolygonOffset**:

-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ POLYGON OFFSET \_ \_ FACTOR
-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ POLYGON OFFSET \_ \_ UNITS
-   [**glIsEnabled con**](glisenabled.md) el argumento GL \_ POLYGON OFFSET \_ \_ FILL
-   [**glIsEnabled con**](glisenabled.md) el argumento GL \_ POLYGON OFFSET \_ \_ LINE
-   [**glIsEnabled con**](glisenabled.md) el argumento GL \_ POLYGON OFFSET \_ \_ POINT

> [!Note]  
> La **función glPolygonOffset** solo está disponible en OpenGl versión 1.1 o posterior.

 

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





