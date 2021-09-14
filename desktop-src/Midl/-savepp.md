---
title: Modificador /savePP
description: Cuando se especifica la directiva /savePP, el compilador midl no elimina la salida del preprocesador de C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP switch MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159710"
---
# <a name="savepp-switch"></a>Modificador /savePP

Cuando se **especifica la directiva /savePP,** el compilador midl no elimina la salida del preprocesador de C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este modificador permite a los desarrolladores distinguir lo que está analizando el compilador midl y es útil para la depuración. La salida del preprocesador se escribe en uno o varios archivos temporales en el directorio indicado por la variable de entorno TEMP. El nombre del archivo de salida, o archivos, sigue una convención de nomenclatura de MID \* .tmp. Tenga en cuenta que una sola compilación puede generar varios flujos de entrada preprocesados; Esto se debe a que la importación de un archivo IDL, en lugar de usar **\# ,** provoca una ejecución de preprocesador independiente.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/no \_ cpp, /nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




