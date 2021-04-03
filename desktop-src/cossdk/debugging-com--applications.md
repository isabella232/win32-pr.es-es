---
description: Las técnicas de depuración para aplicaciones COM+ dependen del idioma en el que decida escribir el componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Depurar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807801"
---
# <a name="debugging-com-applications"></a>Depurar aplicaciones COM+

Las técnicas de depuración para aplicaciones COM+ dependen del idioma en el que decida escribir el componente.

Si codifica en Microsoft Visual C++, puede iniciar el depurador en C++ o, con un cliente remoto, puede depurar mediante el control de procedimiento remoto OLE (RPC) y la depuración Just-in-Time (JIT). Siempre puede usar la herramienta administrativa Servicios de componentes para depurar el componente con la opción **Inicio del depurador** de com+ en la pestaña **Opciones avanzadas** del cuadro de diálogo **propiedades** de la aplicación com+. Para obtener más información sobre la depuración de componentes codificados en C++, vea [depurar componentes escritos en Visual C++](debugging-components-written-in-visual-c--.md).

A menos que esté depurando actualmente multithreading, seguimiento de componentes, llamadas remotas o aislamiento de procesos, puede usar el entorno de Microsoft Visual Basic para fines de depuración. Los [componentes de depuración escritos en Visual Basic](debugging-components-written-in-visual-basic.md) describen el proceso de depuración dentro de un entorno de Visual Basic.

En el tema [depuración del IDE de Visual Basic](debugging-in-the-visual-basic-ide.md) se proporciona información general con instrucciones, sugerencias y un procedimiento para depurar en el entorno de desarrollo integrado (IDE) de.

Para obtener más información sobre la depuración de procesos avanzados, vea [depurar componentes compilados de Visual Basic](debugging-compiled-visual-basic-components.md).

> [!Note]  
> Se han resuelto varias limitaciones relacionadas con el uso del entorno de Visual Basic para depurar componentes con MTS para COM+. Para obtener más información, consulte [compatibilidad con la depuración de COM+ Visual Basic en contraste con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 



