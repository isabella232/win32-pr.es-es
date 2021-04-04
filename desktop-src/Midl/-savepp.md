---
title: modificador/savePP
description: Cuando se especifica la Directiva/savePP, el compilador MIDL no elimina el resultado del preprocesador de C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP modificador MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076767"
---
# <a name="savepp-switch"></a>modificador/savePP

Cuando se especifica la directiva **/savePP** , el compilador MIDL no elimina el resultado del preprocesador de C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este modificador permite a los desarrolladores discernir lo que está analizando el compilador de MIDL y es útil para la depuración. La salida del preprocesador se escribe en uno o varios archivos temporales en el directorio indicado por la variable de entorno TEMP. El nombre del archivo de salida o archivos sigue una Convención de nomenclatura de MID \* . tmp. Tenga en cuenta que una sola compilación puede generar varios flujos de entrada preprocesados. Esto se debe a que la importación de un archivo IDL, en contraposición al uso de **\# include**, provoca una ejecución de preprocesador independiente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ OPC**](-cpp-opt.md)
</dt> <dt>

[/no \_ CPP,/nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




