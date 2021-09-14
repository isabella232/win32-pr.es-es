---
description: Una aplicación de servidor COM+ se puede crear como servicio para iniciarse automáticamente durante el inicio del sistema o manualmente mediante activaciones.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configuración de una aplicación de servidor COM+ como aplicación de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160510"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configuración de una aplicación de servidor COM+ como aplicación de servicio

Una aplicación de servidor COM+ se puede crear como servicio para iniciarse automáticamente durante el inicio del sistema o manualmente mediante activaciones. Si el servicio no se inicia, la opción para el control de errores especifica la gravedad del error y determina la acción que se va a realizar. También está disponible la opción para configurar un servicio para que se ejecute como cuenta del sistema local, así como la opción de asignar una cuenta de usuario específica para la que se ejecutará la aplicación de servidor COM+. También se pueden seleccionar dependencias de una lista de servicios registrados en el equipo mediante Servicios de componentes. Esto determinará qué servicios se deben ejecutar antes de iniciar este servicio.

**Para configurar una aplicación COM+ para que se ejecute como servicio**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación de servidor COM+ que desea ejecutar como servicio.

2.  Haga clic con el botón derecho en la aplicación de servidor COM+ y, a continuación, haga clic en **Propiedades**.

3.  En el cuadro **de** diálogo Propiedades , haga clic en **la pestaña** Activación .

4.  En la **casilla Tipo de** activación, active la casilla Ejecutar aplicación como servicio **NT.**

    > [!Note]  
    > La **casilla Ejecutar aplicación como servicio NT** solo está habilitada para las aplicaciones de servidor y está deshabilitada para las aplicaciones de biblioteca.

     

5.  Haga clic en **el botón Configurar nuevo** servicio.

6.  En el **cuadro Tipo de** inicio del cuadro de diálogo **Nombre** del servicio, **seleccione Automático** o **Manual.**

7.  (Opcional) Para especificar la acción que se va a realizar para un error determinado, seleccione **Omitir**, **Normal,** Grave o Crítico **en** el cuadro **Control de** errores. El comportamiento asociado a cada opción es el siguiente:

    1.  **Ignore**. El programa de inicio registra el error, pero continúa la operación de inicio.
    2.  **Normal.** Se registra el error, se muestra un cuadro de mensaje y el programa de inicio continúa la operación de inicio.
    3.  **Grave.** El error se registra y el sistema se reinicia con la última configuración correcta conocida. Si es la última configuración correcta conocida que se inicia cuando se registra el error, la operación de inicio continúa.
    4.  **Critica**. El error se registra y el sistema se reinicia con la última configuración correcta conocida. Si es la última configuración correcta conocida que se inicia cuando se registra el error, se produce un error en la operación de inicio.

8.  (Opcional) Para establecer otros servicios como dependientes, seleccione los servicios dependientes en la lista en el **cuadro** Dependencias .

9.  (Opcional) Para indicar que se debe permitir que el servicio interactúe con el escritorio, active la casilla Permitir que el servicio **interactúe con el** escritorio.

10. Haga clic en **Crear**.

11. (Opcional) Para asignar el servicio a una cuenta de usuario:

    1.  En la **pestaña Identidad,** seleccione **Este usuario.**
    2.  Para seleccionar el usuario, escriba el nombre de usuario en el **cuadro Usuario** o haga clic en **el botón** Examinar.
    3.  Escriba la contraseña de la cuenta de usuario en el **cuadro Contraseña.**
    4.  Escriba la misma contraseña en el **cuadro Confirmar** contraseña.

 

 



