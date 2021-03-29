---
title: Acerca del administrador de reinicio
description: La principal razón por la que la instalación de software y las actualizaciones requieren un reinicio del sistema es que algunos de los archivos que se están actualizando se están usando actualmente en una aplicación o servicio en ejecución.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Admin. de reinicio del administrador, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793330"
---
# <a name="about-restart-manager"></a>Acerca del administrador de reinicio

La principal razón por la que la instalación de software y las actualizaciones requieren un reinicio del sistema es que algunos de los archivos que se están actualizando se están usando actualmente en una aplicación o servicio en ejecución. El administrador de reinicio permite que todos los servicios y aplicaciones críticas se cierren y se reinicien. Esto libera los archivos que se están usando y permite que se completen las operaciones de instalación. También puede eliminar o reducir el número de reinicios del sistema necesarios para completar una instalación o una actualización.

El administrador de reinicio detiene las aplicaciones en el orden siguiente y, una vez actualizadas las aplicaciones, reinicia las aplicaciones que se han registrado para el reinicio en orden inverso.

1.  Aplicaciones GUI
2.  Aplicaciones de consola
3.  Servicios de Windows
4.  Explorador de Windows

El administrador de reinicio cierra la aplicación o los servicios solo si el autor de la llamada tiene permiso para hacerlo. Tenga en cuenta que no se admite el apagado entre sesiones.

Las aplicaciones que utilizan la [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4,0 para la instalación y el mantenimiento usan automáticamente el administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también pueden diseñarse para que llamen a la API del administrador de reinicio para apagar y reiniciar las aplicaciones y los servicios. En los casos en los que no se puede evitar el reinicio del sistema, los instaladores pueden usar la API del administrador de reinicio para programar los reinicios de forma que se minimice la interrupción del flujo de trabajo del usuario.

Para obtener información acerca del uso de la API del administrador de reinicio durante la instalación y las actualizaciones, consulte [uso del administrador de reinicio](using-restart-manager.md).

El administrador de reinicio no puede detener y reiniciar los servicios críticos del sistema sin necesidad de reiniciar el sistema. Para obtener más información acerca de la identificación de los servicios críticos del sistema, consulte [servicios críticos del sistema](critical-system-services.md).

Las aplicaciones y los servicios deben estar preparados para que los cierre el administrador de reinicio y guarden los datos de usuario y la información de estado que se necesitan para un reinicio limpio. Para obtener más información sobre cómo preparar las aplicaciones y los servicios para que funcionen con el administrador de reinicio, consulte [directrices para aplicaciones y servicios](guidelines-for-applications-and-services.md).

Para obtener información de referencia sobre las enumeraciones, estructuras y funciones de la API del administrador de reinicio, consulte la sección [Referencia del administrador de reinicio](restart-manager-reference.md)

 

 