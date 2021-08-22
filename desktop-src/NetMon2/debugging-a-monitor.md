---
description: En el procedimiento siguiente se muestra cómo depurar un monitor.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Depuración de un monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7ce15252470b280a988f81fe221218778a0fa5e4851db0d3e419d1653fbe92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144208"
---
# <a name="debugging-a-monitor"></a>Depuración de un monitor

En el procedimiento siguiente se muestra cómo depurar un monitor.

**Para depurar un monitor**

1.  Instale la DLL de monitor y el archivo de base de datos de programa (.pdb) generados al compilar el monitor en la ubicación correcta. Consulte [Instalación de un monitor Monitor de red](installing-a-monitor-to-network-monitor.md) para obtener más detalles.
2.  Compruebe que monitor control service está configurado como un servidor en lugar de un servicio seleccionando Panel de control, Servicios.
3.  Abra un símbolo del sistema y vaya al Monitor de red. Escriba:

    **Mcsvc.exe /RegServer**

    Una vez completada la sesión de depuración del monitor, puede devolver MCSVC a su condición predeterminada escribiendo:

    **Mcsvc.exe /Service**

4.  En Microsoft Visual Studio, inicie Microsoft Visual C++.
5.  En la **opción de** **menú** Archivo , Abrir , seleccione el nombre de la DLL del monitor.
6.  Después Microsoft Visual C++ carga, haga clic **en Project**, **Configuración**.
7.  Haga clic en **la pestaña** Depurar en **Ejecutable** para la sesión de depuración y escriba la ruta de acceso completa Mcsvc.exe. Por ejemplo, C: \\ Archivos de programa \\ Netmon2 \\Mcsvc.exe.
8.  Establezca los puntos de interrupción en el código.

> [!Note]  
> No use un cuadro de mensaje para supervisar la depuración. Si MCSVC se ejecuta como un servicio, no verá el elemento emergente y MCSVC parecerá que se ha bloqueado.

 

 

 



