---
title: Modificador /OS
description: El modificador /Os especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /Os switch MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b5e36984783369c96b331af55adac0c97eb8cc2688829d87f7b6d2cea0d7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895945"
---
# <a name="os-switch"></a>Modificador /OS

El **modificador /Os** especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Hay problemas importantes que se deben tener en cuenta antes de decidir el método para serializar código. Estos problemas se refieren al tamaño y el rendimiento. El compilador MIDL proporciona dos métodos para serializar código: modo mixto (**/Os**) y totalmente interpretado ([**/Oi**](-oi.md)). El método totalmente interpretado serializa los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento.

Use el modo predeterminado midl **/Oicf** /robust para todos los propósitos, aparte de la compatibilidad con versiones anteriores. Este modo es el modo estándar seguro del compilador MIDL; cualquier otro modo debe usarse solo después de tener en cuenta detenidamente la implicación de seguridad, al darse cuenta de que las extensiones futuras solo se implementarán para el modo predeterminado. En modo mixto, el compilador serializa algunos parámetros en línea en los códigos auxiliares generados. Aunque esto da como resultado un tamaño de código auxiliar mayor, también puede ofrecer un mayor rendimiento.

MIDL proporciona compatibilidad completa con matrices multidimensionales y punteros de tamaño multidimensional solo en [**modo /Oicf.**](-oi.md) En **los modos /Os** y **/Oi,** el compilador admite casos sencillos, como matrices de tamaño fijo. El uso de matrices multidimensionales en los modos **/Os** o **/Oi** puede dar lugar a parámetros que no se serializan correctamente. Microsoft recomienda usar el modificador de línea de comandos **/Oicf** cuando la interfaz define parámetros que son matrices multidimensionales o punteros de tamaño multidimensional.

Para definir aún más el nivel de gradación en la forma en que se serializan los datos, esta versión de RPC proporciona un \[ [**atributo optimize.**](optimize.md) \] Este atributo se usa como atributo de interfaz ACF u atributo de operación para seleccionar el modo de serialización.

## <a name="examples"></a>Ejemplos

**midl /Os filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 




