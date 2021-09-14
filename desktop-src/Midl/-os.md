---
title: Modificador /Os
description: El modificador /Os especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- Modificador /Os MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159726"
---
# <a name="os-switch"></a>Modificador /Os

El **modificador /Os** especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Hay problemas importantes que se deben tener en cuenta antes de decidir el método para serializar el código. Estos problemas se refieren al tamaño y el rendimiento. El compilador MIDL proporciona dos métodos para serializar código: modo mixto (**/Os**) y totalmente interpretado ([**/Oi**](-oi.md)). El método totalmente interpretado serializa los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento.

Use el modo predeterminado MIDL **/Oicf** /robust para todos los propósitos, aparte de la compatibilidad con versiones anteriores. Este modo es el modo estándar seguro del compilador MIDL; cualquier otro modo debe usarse solo después de tener en cuenta cuidadosamente la implicación de seguridad, al darse cuenta de que las extensiones futuras solo se implementarán para el modo predeterminado. En modo mixto, el compilador serializa algunos parámetros en línea en los códigos auxiliares generados. Aunque esto da como resultado un tamaño de código auxiliar mayor, también puede ofrecer un mayor rendimiento.

MIDL proporciona compatibilidad completa con matrices multidimensionales y punteros de tamaño multidimensional solo en [**modo /Oicf.**](-oi.md) En **los modos /Os** y **/Oi,** el compilador admite casos sencillos, como matrices de tamaño fijo. El uso de matrices multidimensionales en los modos **/Os** o **/Oi** puede dar lugar a parámetros que no se serializan correctamente. Microsoft recomienda usar el modificador de línea de comandos **/Oicf** cuando la interfaz define parámetros que son matrices multidimensionales o punteros de tamaño multidimensional.

Para definir aún más el nivel de gradación en la forma en que se serializan los datos, esta versión de RPC proporciona un \[ [**atributo optimize.**](optimize.md) \] Este atributo se usa como atributo de interfaz ACF o atributo de operación para seleccionar el modo de serialización.

## <a name="examples"></a>Ejemplos

**midl /Os filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 




