---
description: En el siguiente procedimiento se muestra cómo depurar un monitor.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Depurar un monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545382"
---
# <a name="debugging-a-monitor"></a>Depurar un monitor

En el siguiente procedimiento se muestra cómo depurar un monitor.

**Para depurar un monitor**

1.  Instale el archivo DLL del monitor y el archivo de base de datos de programa (. pdb) que se genera al compilar el monitor en la ubicación correcta. Consulte [instalación de un monitor en monitor de red](installing-a-monitor-to-network-monitor.md) para obtener más detalles.
2.  Compruebe que el servicio de control de supervisión está configurado como un servidor en lugar de un servicio seleccionando panel de control, servicios.
3.  Abra un símbolo del sistema y vaya al directorio Monitor de red. Escriba:

    **Mcsvc.exe/RegServer**

    Una vez completada la sesión de depuración del monitor, puede devolver el valor de MCSVC a su condición predeterminada; para ello, escriba:

    **Mcsvc.exe/Service**

4.  En Microsoft Visual Studio, Inicie Microsoft Visual C++.
5.  En la opción de menú **archivo**, **abrir** , seleccione el nombre de la dll del monitor.
6.  Después de cargar Microsoft Visual C++, haga clic en **proyecto**, **configuración**.
7.  Haga clic en la pestaña **depurar** en **ejecutable** para sesión de depuración y escriba la ruta de acceso completa de Mcsvc.exe. Por ejemplo, C: \\ archivos de programa \\ Netmon2 \\Mcsvc.exe.
8.  Establezca los puntos de interrupción en el código.

> [!Note]  
> No use un cuadro de mensaje para la depuración de monitores. Si el MCSVC se ejecuta como un servicio, no verá el elemento emergente y MCSVC parecerá que deja de responder.

 

 

 



