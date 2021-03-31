---
description: Dado que en muchos casos podrá depurar solo una parte de la funcionalidad de los componentes dentro del entorno de Microsoft Visual Basic, habrá situaciones en las que necesitará depurar componentes compilados con Visual Basic una vez que se hayan compilado. Como el entorno de Visual Basic no lo habilita, en su lugar debe usar el entorno de Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depurar componentes Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153066"
---
# <a name="debugging-compiled-visual-basic-components"></a>Depurar componentes Visual Basic compilados

Dado que en muchos casos solo podrá depurar una parte de la funcionalidad del componente en el entorno de Microsoft Visual Basic, habrá situaciones en las que necesitará depurar los componentes compilados con Visual Basic una vez que se hayan compilado. Como el entorno de Visual Basic no lo habilita, en su lugar debe usar el entorno de Microsoft Visual C++.

**Para depurar un componente de Visual Basic en el entorno de Visual C++**

1.  En Visual Basic 6,0, abra el proyecto de Visual Basic que desea depurar.

2.  En el menú **archivo** , haga clic en **crear YourProject.dll**.

3.  En el cuadro de diálogo **crear proyecto** , haga clic en **Opciones**.

4.  En el cuadro de diálogo **propiedades del proyecto** , en la pestaña **compilar** , haga clic en **compilar en código nativo** y **sin optimización** y seleccione la casilla **crear información de depuración simbólica** .

5.  Haga clic en **Aceptar** y, a continuación, haga clic en **Aceptar** de nuevo para compilar el proyecto.

6.  Mueva la DLL compilada a la ubicación donde se instalan normalmente las aplicaciones COM+.

    > [!Note]  
    > Si no mueve el archivo DLL, es posible que reciba un mensaje de error que le informa de que no se pudo encontrar la información de depuración simbólica de la DLL. Si tiene problemas para que el depurador se detenga en los puntos de interrupción del componente, confirme que el archivo DLL está en el directorio de paquetes estándar, elimine el componente de su paquete y vuelva a agregar el componente.

     

7.  Inicie Visual C++.

8.  En el menú **archivo** , haga clic en **abrir área de trabajo**.

9.  En el cuadro de diálogo **abrir área de trabajo** , establezca **archivos de tipo** en **todos los archivos ( \* . \* )**, seleccione el componente compilado y haga clic en **abrir**.

10. En el menú **archivo** , haga clic en **abrir** (no **abrir área de trabajo**) y abra el módulo de Visual Basic (. Bas), el formulario (. FRM) o la clase (. CLS) que desea depurar.

11. En el menú **proyecto** , haga clic en **configuración**.

12. En el cuadro de diálogo **configuración del proyecto** , en la pestaña **depurar** , seleccione **General** en el cuadro **categoría** .

13. En el cuadro **ejecutable para sesión de depuración** , escriba la ruta de acceso completa de Dllhost.exe, seguido de un argumento que especifique el ID. de proceso de la aplicación com+ que contiene el componente. Encontrará el identificador de proceso en la pestaña **General** del cuadro de diálogo **propiedades** de la aplicación com+. A continuación se encuentra un ejemplo: C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: { <processID> }.

14. Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depuración en el IDE de Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



