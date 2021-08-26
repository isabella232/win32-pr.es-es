---
description: Depuración de componentes escritos en Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Depuración de componentes escritos en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991185"
---
# <a name="debugging-components-written-in-visual-basic"></a>Depuración de componentes escritos en Visual Basic

Puede usar el entorno de desarrollo de Microsoft Visual Basic 6.0 para la depuración en determinados escenarios. El Visual Basic para la depuración permite el acceso a herramientas familiares para Visual Basic programadores. Por otro lado, dado que durante la depuración, los componentes de Visual Basic se ejecutan dentro del proceso del entorno de Visual Basic, puede ser necesario depurar el componente una vez compilado mediante el entorno de desarrollo Microsoft Visual C++.

Para obtener más información sobre la depuración en Visual Basic entorno de desarrollo integrado (IDE), vea [Depuración](debugging-in-the-visual-basic-ide.md)en el IDE Visual Basic . Para obtener más información sobre la depuración Visual Basic componentes después de compilarse mediante el entorno de desarrollo de Visual C++, vea Depuración de componentes Visual Basic [compilados.](debugging-compiled-visual-basic-components.md)

Además, se han resuelto varias limitaciones asociadas al uso del Visual Basic de depuración de componentes con MTS para COM+. Para obtener más información, [vea COM+ Visual Basic de depuración contrastada con MTS.](com--visual-basic-debugging-support-contrasted-with-mts.md)

> [!Note]  
> Si ya ha usado Visual Basic en el mismo equipo que COM+, es posible que haya observado que el complemento Servicios de componentes está disponible en el entorno de Visual Basic. Originalmente en MTS, esta característica se diseñó para actualizar el registro cada vez que se vuelve a compilar un componente en una aplicación COM+. Sin embargo, dada la naturaleza de la interacción de Microsoft Windows Registry y la base de datos de registro de COM+, es posible que algunas configuraciones no se actualicen por completo. Por lo tanto, en lugar de usar los comandos disponibles con este complemento, debe quitar y reinstalar los componentes para actualizar la configuración después de volver a compilar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración de componentes escritos en Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



