---
description: Use el procedimiento siguiente para depurar expertos escritos en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depuración de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260508"
---
# <a name="debugging-an-expert"></a>Depuración de un experto

Use el procedimiento siguiente para depurar expertos escritos en Microsoft Visual C++.

**Depuración de un experto**

1.  Instale el experto (archivo DLL) y el archivo de base de datos de programa (.pdb) generados al compilar el experto en la ubicación correcta. Para obtener más información, vea [Installing an Expert to Monitor de red 2.1](installing-an-expert-to-network-monitor-2-1.md).
2.  Inicie Microsoft Visual C++.
3.  En el **menú Archivo,** haga clic **en Abrir** y seleccione el nombre del archivo DLL experto.
4.  Después de Microsoft Visual C++ carga, haga clic en **el menú Project** y, a continuación, haga clic **Configuración**.
5.  Haga clic **en Depurar**. En **Ejecutable para la sesión de depuración**, escriba la ruta de acceso completa Netmon.exe, por ejemplo:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Establezca los puntos de interrupción en el código.

 

 



