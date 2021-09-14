---
description: Información general de los controles de entrada de lápiz para tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Controles de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262396"
---
# <a name="ink-controls"></a>Controles de entrada de lápiz

La plataforma tablet PC proporciona dos controles, [InkEdit](inkedit-control.md) y [InkPicture,](inkpicture-control.md)que le permiten agregar fácilmente reconocimiento de escritura a mano y entrada de lápiz a las aplicaciones de Tablet PC. El control InkEdit ha administrado [,](/previous-versions/ms835842(v=msdn.10)) [ActiveX](inkedit-control-reference.md) y las versiones win32, mientras que InkPicture solo tiene las versiones [inkPicture](/previous-versions/ms583740(v=vs.100)) [y ActiveX](inkpicture-control-reference.md) administradas.

La diferencia clave entre los controles está en cómo se guardan los datos. El control [InkEdit](inkedit-control.md) guarda la entrada de lápiz como texto de forma predeterminada, mientras [que InkPicture](inkpicture-control.md) guarda la entrada de lápiz como entrada de lápiz.

El [control InkEdit](inkedit-control.md) está pensado para la entrada de texto a través del reconocimiento de escritura a mano. [InkPicture está](inkpicture-control.md) pensado para anotaciones (por ejemplo, marcar una diapositiva de presentación u otra imagen).

En código administrado, cree controles de entrada de lápiz en el mismo subproceso que el subproceso principal del formulario. Si se crea un control [InkEdit](inkedit-control.md) o [InkPicture](inkpicture-control.md) en un subproceso diferente, es posible que la aplicación no responda correctamente.

Debe cambiar explícitamente el modelo de subprocesos a un único apartamento de subproceso (STA) antes de crear un control de entrada de lápiz. Esto hace que el control se cree en el subproceso principal. Puede usar el siguiente código de C++ administrado para establecer explícitamente el modelo de subprocesos.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Puede usar el código siguiente para hacer lo mismo en C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



En código administrado, para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier control de Tablet PC al que se haya asociado un controlador de eventos antes de que el control salga del ámbito.

En las secciones siguientes se describen los controles de entrada de lápiz y el uso de controles de entrada de lápiz en las aplicaciones:

-   [Agregar controles ink a un Project](adding-ink-controls-to-a-project.md)
-   [InkEdit Control](inkedit-control.md)
-   [InkPicture Control](inkpicture-control.md)

 

 
