---
description: Depurar componentes escritos en Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Depurar componentes escritos en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705375"
---
# <a name="debugging-components-written-in-visual-basic"></a>Depurar componentes escritos en Visual Basic

Puede usar el entorno de desarrollo de Microsoft Visual Basic 6,0 para la depuración en ciertos escenarios. El uso de Visual Basic para la depuración permite el acceso a herramientas conocidas para los programadores de Visual Basic. Por otro lado, dado que durante la depuración Visual Basic componentes se ejecutan dentro del proceso del entorno de Visual Basic, puede que sea necesario depurar el componente una vez compilado con el entorno de desarrollo de Microsoft Visual C++.

Para obtener más información sobre la depuración en el entorno de desarrollo integrado (IDE) de Visual Basic, consulte [depuración en el IDE de Visual Basic](debugging-in-the-visual-basic-ide.md). Para obtener más información sobre la depuración de componentes Visual Basic una vez compilados con el entorno de desarrollo de Visual C++, vea [depurar componentes Compilados Visual Basic](debugging-compiled-visual-basic-components.md).

Además, se han resuelto varias limitaciones asociadas al uso del entorno de Visual Basic para depurar componentes con MTS para COM+. Para obtener más información, consulte [compatibilidad con la depuración de COM+ Visual Basic en contraste con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> Si ya ha usado Visual Basic en el mismo equipo que COM+, es posible que haya observado que el complemento Servicios de componentes está disponible en el entorno de Visual Basic. Originalmente en MTS, esta característica se diseñó para actualizar el registro cada vez que se volvió a compilar un componente en una aplicación COM+. Sin embargo, dada la naturaleza de la interacción del registro de Microsoft Windows y la base de datos de registro de COM+, es posible que algunas configuraciones no se actualicen por completo. Por lo tanto, en lugar de usar los comandos disponibles con este complemento, debe quitar y volver a instalar los componentes para actualizar la configuración después de volver a compilar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar componentes escritos en Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



