---
title: Acerca del Administrador de reinicio
description: La razón principal por la que la instalación y las actualizaciones de software requieren un reinicio del sistema es que algunos de los archivos que se están actualizando están siendo usados actualmente por una aplicación o servicio en ejecución.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Restart Manager Restart Mgr , about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98003ff4193ce26eb4ed2a3bdab60db8d58adf86698c6b9369a80b8043458579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010303"
---
# <a name="about-restart-manager"></a>Acerca del Administrador de reinicio

La razón principal por la que la instalación y las actualizaciones de software requieren un reinicio del sistema es que algunos de los archivos que se están actualizando están siendo usados actualmente por una aplicación o servicio en ejecución. Restart Manager permite apagar y reiniciar todas las aplicaciones y servicios críticos, menos . Esto libera los archivos que están en uso y permite que se completen las operaciones de instalación. También puede eliminar o reducir el número de reinicios del sistema necesarios para completar una instalación o actualización.

El Administrador de reinicio detiene las aplicaciones en el orden siguiente y, una vez actualizadas las aplicaciones, reinicia las aplicaciones que se han registrado para reiniciarse en orden inverso.

1.  Aplicaciones gui
2.  Aplicaciones de consola
3.  Servicios de Windows
4.  Windows explorador

Restart Manager cierra la aplicación o los servicios solo si el autor de la llamada tiene permiso para hacerlo. Tenga en cuenta que no se admite el apagado entre sesiones.

Las aplicaciones que usan [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4.0 para la instalación y el mantenimiento usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también se pueden diseñar para llamar a la API de Restart Manager para apagar y reiniciar aplicaciones y servicios. En los casos en los que un reinicio del sistema es inevitable, los instaladores pueden usar la API de Restart Manager para programar reinicios de forma que minimice la interrupción del flujo de trabajo del usuario.

Para obtener información sobre el uso de la API de Restart Manager durante la instalación y las actualizaciones, vea [Using Restart Manager](using-restart-manager.md).

El Administrador de reinicio no puede detener ni reiniciar los servicios críticos del sistema sin un reinicio del sistema. Para obtener más información sobre cómo identificar servicios críticos del sistema, vea [Critical System Services](critical-system-services.md).

Las aplicaciones y los servicios deben estar preparados para que el Administrador de reinicio lo apague y guardar los datos de usuario y la información de estado necesarios para un reinicio limpio. Para obtener más información sobre cómo preparar las aplicaciones y los servicios para que funcionen con el Administrador de reinicio, vea [Directrices para aplicaciones y servicios.](guidelines-for-applications-and-services.md)

Para obtener información de referencia sobre las enumeraciones, estructuras y funciones de la API de Restart Manager, consulte la sección [Referencia de Restart Manager.](restart-manager-reference.md)

 

 