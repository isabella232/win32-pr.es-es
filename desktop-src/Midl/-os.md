---
title: Parámetro/os
description: El modificador/os especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /Os (modificador) MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676289"
---
# <a name="os-switch"></a>Parámetro/os

El modificador **/os** especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Hay problemas importantes que se deben tener en cuenta antes de decidir el método para calcular las referencias del código. Estos problemas están relacionados con el tamaño y el rendimiento. El compilador MIDL proporciona dos métodos para calcular las referencias del código: modo mixto (**/os**) y totalmente interpretado ([**/OI**](-oi.md)). El método totalmente interpretado calcula las referencias de los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento.

Use el modo predeterminado de MIDL **/Oicf** /Robust para todos los fines distintos de la compatibilidad con versiones anteriores. Este modo es el modo estándar seguro del compilador MIDL; cualquier otro modo se debe usar solo después de haber tenido cuidado en la implicación de la seguridad, de modo que las extensiones futuras solo se implementarán para el modo predeterminado. En el modo mixto, el compilador calcula las referencias de algunos parámetros insertados en el código auxiliar generado. Aunque esto da como resultado un mayor tamaño de código auxiliar, también puede ofrecer mayor rendimiento.

MIDL proporciona compatibilidad total con las matrices multidimensionales y los punteros de tamaño multidimensional solo en modo [**/Oicf**](-oi.md) . En los modos **/os** y **/OI** , el compilador admite casos sencillos, como matrices de tamaño fijo. El uso de matrices multidimensionales en los modos **/os** o **/OI** puede dar lugar a parámetros cuyas referencias no se han calculado correctamente. Microsoft recomienda que use el modificador de la línea de comandos **/Oicf** cuando la interfaz defina parámetros que son matrices multidimensionales o punteros de tamaño multidimensional.

Para definir con mayor precisión el nivel de degradado en la forma en que se calculan las referencias de los datos, esta versión de RPC proporciona un \[ atributo [**Optimize**](optimize.md) \] . Este atributo se usa como atributo de interfaz ACF u operación para seleccionar el modo de cálculo de referencias.

## <a name="examples"></a>Ejemplos

**MIDL/os FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**optimiz**](optimize.md)
</dt> <dt>

[**/no \_ format \_ OPC**](-no-format-opt.md)
</dt> </dl>

 

 




