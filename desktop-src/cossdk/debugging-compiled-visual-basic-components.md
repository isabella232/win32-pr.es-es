---
description: Dado que en muchos casos solo podrá depurar una parte de la funcionalidad de los componentes en el entorno de Microsoft Visual Basic, habrá situaciones en las que deberá depurar los componentes compilados con Visual Basic después de que se hayan compilado. Como el Visual Basic no lo habilita, en su lugar debe usar el Microsoft Visual C++ de trabajo.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depuración de componentes Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2dec15f90d14d534221193020417415d11ddec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882988"
---
# <a name="debugging-compiled-visual-basic-components"></a>Depuración de componentes Visual Basic compilados

Dado que en muchos casos solo podrá depurar una parte de la funcionalidad del componente en el entorno de Microsoft Visual Basic, habrá situaciones en las que deberá depurar los componentes compilados con Visual Basic después de que se hayan compilado. Como el Visual Basic no lo habilita, en su lugar debe usar el Microsoft Visual C++ de trabajo.

**Para depurar un componente Visual Basic en el Visual C++ de depuración**

1.  En Visual Basic 6.0, abra el Visual Basic proyecto que desea depurar.

2.  En el **menú Archivo** , haga clic en **Crear YourProject.dll**.

3.  En el **cuadro de diálogo Crear Project,** haga clic en **Opciones**.

4.  En el **cuadro Project propiedades,** en  la pestaña  Compilar ,  haga clic en Compilar en código nativo y sin optimización y active la casilla Crear información de **depuración** simbólica.

5.  Haga **clic en Aceptar** y, a continuación, en **Aceptar** de nuevo para compilar el proyecto.

6.  Mueva el archivo DLL compilado a la ubicación donde normalmente se instalan las aplicaciones COM+.

    > [!Note]  
    > Si no mueve el archivo DLL, puede recibir un mensaje de error que le informa de que no se pudo encontrar información de depuración simbólica para el archivo DLL. Si tiene problemas para que el depurador se detenga en los puntos de interrupción del componente, confirme que el archivo DLL está en el directorio de paquetes estándar, elimine el componente de su paquete y vuelva a agregar el componente.

     

7.  Inicie Visual C++.

8.  En el menú **Archivo ,** haga clic en Abrir área **de trabajo.**

9.  En el **cuadro de diálogo Abrir** área de trabajo, establezca **Archivos** de tipo en Todos los **archivos( \* . \* )**, seleccione el componente compilado y haga clic **en Abrir**.

10. En el menú **Archivo,** haga clic en Abrir **(no** Abrir área de **trabajo)** y abra el módulo de Visual Basic (.bas), el formulario (.frm) o la clase (.cls) que desea depurar.

11. En el menú **Project,** haga clic **en Configuración**.

12. En el **Project Configuración** de diálogo, en la **pestaña Depurar** , seleccione **General** en el **cuadro** Categoría .

13. En el **cuadro Sesión** ejecutable para depuración, escriba la ruta de acceso completa para Dllhost.exe, seguida de un argumento que especifique el identificador de proceso de la aplicación COM+ que contiene el componente. Encontrará el identificador de proceso en la **pestaña** General  del cuadro de diálogo Propiedades de la aplicación COM+. A continuación se muestra un ejemplo: C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{ &lt; processID &gt; }.

14. Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con Visual Basic depuración de COM+ contrastada con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depuración en el IDE de Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



