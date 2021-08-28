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
ms.openlocfilehash: c574d1032d9e392973478bc1df1e22cde6a49145b6f4775d928aac0b35e6988b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067485"
---
# <a name="savepp-switch"></a>Modificador /savePP

Cuando se **especifica la directiva /savePP,** el compilador midl no elimina la salida del preprocesador de C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Este modificador permite a los desarrolladores distinguir lo que está analizando el compilador midl y es útil para la depuración. La salida del preprocesador se escribe en uno o varios archivos temporales en el directorio indicado por la variable de entorno TEMP. El nombre del archivo de salida, o archivos, sigue una convención de nomenclatura de MID \* .tmp. Tenga en cuenta que una sola compilación puede generar varios flujos de entrada preprocesados; Esto se debe a que la importación de un archivo IDL, en lugar de usar **\# ,** provoca una ejecución de preprocesador independiente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/no \_ cpp, /nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




