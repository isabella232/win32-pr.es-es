---
description: Se puede crear una aplicación de servidor COM+ como servicio para que se inicie automáticamente durante el inicio del sistema o manualmente mediante las activaciones.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configuración de una aplicación de servidor COM+ como aplicación de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907092"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configuración de una aplicación de servidor COM+ como aplicación de servicio

Se puede crear una aplicación de servidor COM+ como servicio para que se inicie automáticamente durante el inicio del sistema o manualmente mediante las activaciones. Si el servicio no se inicia, la opción para el control de errores especifica la gravedad del error y determina la acción que se va a realizar. También está disponible la opción para configurar un servicio para que se ejecute como la cuenta de sistema local, así como la opción para asignar una cuenta de usuario específica para la que se ejecutará la aplicación de servidor COM+. Las dependencias también se pueden seleccionar en una lista de servicios registrados en el equipo con servicios de componentes. Esto determinará qué servicios deben ejecutarse antes de que se inicie este servicio.

**Para configurar una aplicación COM+ para que se ejecute como un servicio**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación de servidor COM+ que desea ejecutar como servicio.

2.  Haga clic con el botón secundario en la aplicación de servidor COM+ y, a continuación, haga clic en **propiedades**.

3.  En el cuadro de diálogo **propiedades** , haga clic en la pestaña **activación** .

4.  En el cuadro **tipo de activación** , active la casilla **Ejecutar aplicación como servicio NT** .

    > [!Note]  
    > La casilla **Ejecutar aplicación como servicio NT** solo está habilitada para aplicaciones de servidor y está deshabilitada para las aplicaciones de biblioteca.

     

5.  Haga clic en el botón **instalar nuevo servicio** .

6.  En el cuadro **tipo de inicio** del cuadro de diálogo nombre de **servicio** , seleccione **automático** o **manual**.

7.  Opta Para especificar la acción que se va a realizar para un error determinado, seleccione **omitir**, **normal**, **grave** o **crítico** en el cuadro **tratamiento de errores** . El comportamiento asociado a cada opción es el siguiente:

    1.  **Ignore**. El programa de inicio registra el error, pero continúa con la operación de inicio.
    2.  **Normal**. El error se registra, se muestra un cuadro de mensaje y el programa de inicio continúa con la operación de inicio.
    3.  **Grave**. El error se registra y el sistema se reinicia con la última configuración válida conocida. Si se trata de la última configuración válida conocida que se está iniciando cuando se registra el error, la operación de inicio continúa.
    4.  **Critica**. El error se registra y el sistema se reinicia con la última configuración válida conocida. Si se trata de la última configuración válida conocida que se está iniciando cuando se registra el error, se produce un error en la operación de inicio.

8.  Opta Para establecer otros servicios como dependientes, seleccione los servicios dependientes en la lista del cuadro **dependencias** .

9.  Opta Para indicar que se debe permitir que el servicio interactúe con el escritorio, active la casilla permitir que el **servicio interactúe con el escritorio** .

10. Haga clic en **Crear**.

11. Opta Para asignar el servicio a una cuenta de usuario:

    1.  En la pestaña **identidad** , seleccione **este usuario**.
    2.  Para seleccionar el usuario, escriba el nombre de usuario en el cuadro **usuario** o haga clic en el botón **examinar** .
    3.  Escriba la contraseña de la cuenta de usuario en el cuadro **contraseña** .
    4.  Escriba la misma contraseña en el cuadro **Confirmar contraseña** .

 

 



