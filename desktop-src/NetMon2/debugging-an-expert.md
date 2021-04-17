---
description: Utilice el procedimiento siguiente para depurar a los expertos escritos en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depuración de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667734"
---
# <a name="debugging-an-expert"></a>Depuración de un experto

Utilice el procedimiento siguiente para depurar a los expertos escritos en Microsoft Visual C++.

**Depuración de un experto**

1.  Instale el experto (archivo DLL) y el archivo de base de datos de programa (. pdb) que se genera al compilar el experto en la ubicación correcta. Para obtener más información, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Inicie Microsoft Visual C++.
3.  En el menú **archivo** , haga clic en **abrir** y seleccione el nombre de la dll experta.
4.  Después de cargar Microsoft Visual C++, haga clic en el menú **proyecto** y, a continuación, en **configuración**.
5.  Haga clic en **depurar**. En **ejecutable para sesión de depuración**, escriba la ruta de acceso completa de Netmon.exe, por ejemplo:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Establezca los puntos de interrupción en el código.

 

 



