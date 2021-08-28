---
description: Use el procedimiento siguiente para depurar expertos escritos en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depuración de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdd54484d8dc7d36bf1162433fc98d7d72565d9810c7e0ed838e9193510ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064145"
---
# <a name="debugging-an-expert"></a>Depuración de un experto

Use el procedimiento siguiente para depurar expertos escritos en Microsoft Visual C++.

**Depuración de un experto**

1.  Instale el experto (archivo DLL) y el archivo de base de datos de programa (.pdb) generados al compilar el experto en la ubicación correcta. Para obtener más información, vea Installing an Expert to Monitor de red 2.1 (Instalación de un [Monitor de red 2.1).](installing-an-expert-to-network-monitor-2-1.md)
2.  Inicie Microsoft Visual C++.
3.  En el **menú Archivo,** haga clic **en Abrir** y seleccione el nombre del archivo DLL experto.
4.  Después Microsoft Visual C++ cargar, haga clic en **el menú Project** y, a continuación, haga clic **Configuración**.
5.  Haga clic **en Depurar**. En **Ejecutable para la sesión de depuración,** escriba la ruta de acceso completa Netmon.exe, por ejemplo:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Establezca los puntos de interrupción en el código.

 

 



