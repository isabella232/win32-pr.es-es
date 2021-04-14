---
description: Información general de los controles de entrada manuscrita para Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controles de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541315"
---
# <a name="ink-controls"></a>Controles de entrada manuscrita

La plataforma de Tablet PC proporciona dos controles, [InkEdit](inkedit-control.md) y [InkPicture](inkpicture-control.md), que le permiten agregar fácilmente reconocimiento de tinta y escritura a mano a las aplicaciones de Tablet PC. El control InkEdit tiene versiones [administradas](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) y Win32, mientras que InkPicture solo tiene las versiones de [InkPicture](/previous-versions/ms583740(v=vs.100)) y [ActiveX](inkpicture-control-reference.md) administradas.

La diferencia clave entre los controles es cómo se guardan los datos. El control [InkEdit](inkedit-control.md) guarda la entrada manuscrita como texto de forma predeterminada, mientras que [InkPicture](inkpicture-control.md) guarda la tinta como entrada de lápiz.

El control [InkEdit](inkedit-control.md) está destinado a la entrada de texto mediante el reconocimiento de escritura a mano. El formato de [InkPicture](inkpicture-control.md) está diseñado para la anotación (por ejemplo, al marcar una diapositiva de presentación u otra imagen).

En código administrado, cree controles de entrada de lápiz en el mismo subproceso que el subproceso principal del formulario. Si se crea un control [InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) en un subproceso diferente, es posible que la aplicación no responda correctamente.

Debe cambiar explícitamente el modelo de subprocesos a Apartamento de un solo subproceso (STA) antes de crear un control de entrada de lápiz. Esto hace que el control se cree en el subproceso principal. Puede usar el siguiente código de C++ administrado para establecer explícitamente el modelo de subprocesos.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Puede usar el siguiente código para hacer lo mismo en C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



En código administrado, para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el control salga del ámbito.

En las secciones siguientes se describen los controles de entrada manuscrita y el uso de controles de entrada manuscrita en aplicaciones:

-   [Agregar controles de entrada manuscrita a un proyecto](adding-ink-controls-to-a-project.md)
-   [Control InkEdit](inkedit-control.md)
-   [InkPicture (control)](inkpicture-control.md)

 

 
