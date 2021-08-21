---
description: Las técnicas de depuración para aplicaciones COM+ dependen del lenguaje en el que decida escribir el componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Depuración de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcce186a954098bdebd4e7e326328b8be269a88ed9567a3e63185662fcda3d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307321"
---
# <a name="debugging-com-applications"></a>Depuración de aplicaciones COM+

Las técnicas de depuración para aplicaciones COM+ dependen del lenguaje en el que decida escribir el componente.

Si codifica en Microsoft Visual C++, puede iniciar el depurador en C++ o, con un cliente remoto, puede depurar mediante el control de procedimiento remoto OLE (RPC) y la depuración Just-In-Time (JIT). Siempre puede usar la herramienta administrativa Servicios de componentes para depurar el  componente con la opción  Iniciar en el depurador de **COM+** en la pestaña Opciones avanzadas del cuadro de diálogo Propiedades de la aplicación COM+. Para obtener más información sobre la depuración de componentes codificados en C++, vea Depurar componentes [escritos en Visual C++](debugging-components-written-in-visual-c--.md).

A menos que esté depurando actualmente multithreading, seguimiento de componentes, llamadas remotas o aislamiento de procesos, puede usar el entorno de Microsoft Visual Basic con fines de depuración. [Los componentes de depuración escritos Visual Basic](debugging-components-written-in-visual-basic.md) describe el proceso de depuración dentro de un Visual Basic de depuración.

El tema [Depuración](debugging-in-the-visual-basic-ide.md) en el IDE de Visual Basic proporciona información general con instrucciones, sugerencias y un procedimiento sobre la depuración en el entorno de desarrollo integrado (IDE).

Para ver más información sobre la depuración de procesos avanzados, vea Depuración de componentes [Visual Basic compilación](debugging-compiled-visual-basic-components.md).

> [!Note]  
> Se han resuelto varias limitaciones asociadas al uso del Visual Basic para depurar componentes con MTS para COM+. Para obtener más información, [vea COM+ Visual Basic de depuración contrastada con MTS.](com--visual-basic-debugging-support-contrasted-with-mts.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 



