---
description: Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Control de errores con el compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993175"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Control de errores con el compilador MOF

Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido. Por ejemplo, si está compilando un archivo MOF y usa el modificador de línea de comandos **-class:createonly,** la compilación finaliza si ya existe una clase especificada en el archivo MOF. El compilador MOF almacena en el repositorio todas las clases o instancias que se definieron hasta el punto en que se detiene el compilador. En algunos casos, esto puede dejar el repositorio WMI en una condición indefinido.

En esta situación, es posible que tenga que detener WMI, eliminar el repositorio WMI y hacer que WMI lo recompile. Todos los archivos MOF que contienen el [**comando pragma autorecover**](pragma-autorecover.md) [preprocessor](preprocessor-commands.md) se recompila cuando se reinicia WMI. Debe volver a compilar manualmente los archivos MOF que no incluyan una `#pragma autorecover` instrucción .

Para obtener más información sobre cómo declarar clases e instancias mediante la sintaxis MOF, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar archivos MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



