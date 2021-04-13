---
title: función glPolygonOffset (GL. h)
description: La función glPolygonOffset establece la escala y las unidades que usa OpenGL para calcular los valores de profundidad.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset (función) OpenGL
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
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422390"
---
# <a name="glpolygonoffset-function"></a>glPolygonOffset función)

La función **glPolygonOffset** establece la escala y las unidades que usa OpenGL para calcular los valores de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*diez* 
</dt> <dd>

Especifica un factor de escala que se usa para crear un desplazamiento de profundidad variable para cada polígono. El valor inicial es cero.

</dd> <dt>

*participa* 
</dt> <dd>

Especifica un valor que se multiplica por un valor específico de la implementación para crear un desplazamiento de profundidad constante. El valor inicial es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Cuando \_ se habilita el desplazamiento de polígono de GL \_ , el valor de profundidad de cada fragmento se desplazará después de que se interpola a partir de los valores de profundidad de los vértices adecuados. El valor del desplazamiento es *factor* \* ? z + r \* *unidades*, donde? z es una medida del cambio en profundidad en relación con el área de la pantalla del polígono y r es el valor más pequeño que se garantiza para generar un desplazamiento que se pueda resolver para una implementación determinada. El desplazamiento se agrega antes de que se realice la prueba de profundidad y antes de que el valor se escriba en el búfer de profundidad.

La función **glPolygonOffset** es útil para representar imágenes de línea oculta, para aplicar marcas a superficies y para representar sólidos con bordes resaltados.

La función **glPolygonOffset** no tiene ningún efecto en las coordenadas de profundidad colocadas en el búfer de comentarios. Tampoco tiene ningún efecto en la selección.

Las siguientes funciones recuperan información relacionada con **glPolygonOffset**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ el \_ factor de desplazamiento de polígono de contabilidad \_
-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con unidades de \_ desplazamiento de polígono de argumento \_ \_
-   [**glIsEnabled**](glisenabled.md) con argumento de \_ desplazamiento de polígono de contabilidad de argumentos \_ \_
-   [**glIsEnabled**](glisenabled.md) con el argumento \_ de \_ línea de desplazamiento de polígono de contabilidad \_
-   [**glIsEnabled**](glisenabled.md) con el \_ punto de \_ desplazamiento de polígono de contabilidad de argumentos \_

> [!Note]  
> La función **glPolygonOffset** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

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

 

 





