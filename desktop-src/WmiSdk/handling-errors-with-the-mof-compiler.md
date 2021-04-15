---
description: Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Control de errores con el compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498118"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Control de errores con el compilador MOF

Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido. Por ejemplo, si está compilando un archivo MOF y usa el modificador de línea de comandos **-Class: createonly** , la compilación finaliza si ya existe una clase especificada en el archivo MOF. El compilador MOF almacena en el repositorio cualquier clase o instancia que se haya definido hasta el punto en el que se detiene el compilador. En algunos casos, esto puede dejar el repositorio WMI en una condición no definida.

En esta situación, es posible que necesite detener WMI, eliminar el repositorio WMI y hacer que WMI lo Recompile. Todos los archivos MOF que contengan el comando [**pragma autocover**](pragma-autorecover.md) del [preprocesador](preprocessor-commands.md) se vuelven a generar cuando se reinicia WMI. Debe volver a compilar manualmente cualquier archivo MOF que no incluya una `#pragma autorecover` instrucción.

Para obtener más información sobre cómo declarar clases e instancias con la sintaxis MOF, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar archivos MOF](compiling-mof-files.md)
</dt> <dt>

[**MOFCOMP**](mofcomp.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



