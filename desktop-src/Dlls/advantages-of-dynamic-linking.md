---
description: La vinculación dinámica tiene las siguientes ventajas con respecto a la vinculación estática.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Ventajas de la vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a35e254ae14f74d5e2ed4c260f3ee201e2fd1f62efd8aa953b708256e437c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632285"
---
# <a name="advantages-of-dynamic-linking"></a>Ventajas de la vinculación dinámica

La vinculación dinámica tiene las siguientes ventajas con respecto a la vinculación estática:

-   Varios procesos que cargan el mismo archivo DLL en la misma dirección base comparten una única copia del archivo DLL en la memoria física. Al hacerlo, se ahorra memoria del sistema y se reduce el intercambio.
-   Cuando cambian las funciones de un archivo DLL, no es necesario volver a compilar ni volver a vincular las aplicaciones que las usan, siempre y cuando los argumentos de función, las convenciones de llamada y los valores devueltos no cambien. En cambio, el código de un objeto vinculado estáticamente requiere que se vuelva a vincular la aplicación cuando cambien las funciones.
-   Un archivo DLL puede proporcionar soporte técnico posterior al mercado. Por ejemplo, se puede modificar un archivo DLL del controlador de pantalla para admitir una pantalla que no estaba disponible cuando se envió inicialmente la aplicación.
-   Los programas escritos en lenguajes de programación diferentes pueden llamar a la misma función DLL siempre y cuando los programas sigan la misma convención de llamada que usa la función. La convención de llamada (como C, Pascal o la llamada estándar) controla el orden en el que la función que realiza la llamada debe insertar los argumentos en la pila, si la función o la función de llamada son responsables de limpiar la pila y si se pasan argumentos en los registros. Para obtener más información, consulte la documentación incluida con el compilador.

Una posible desventaja de utilizar archivos DLL es que la aplicación no es independiente; depende de la existencia de un módulo de archivo DLL separado. El sistema finaliza los procesos mediante la vinculación dinámica en tiempo de carga si requieren un archivo DLL que no se encuentra en el inicio del proceso y envía un mensaje de error al usuario. El sistema no finaliza un proceso mediante la vinculación dinámica en tiempo de ejecución en esta situación, pero las funciones exportadas por el archivo DLL que falta no están disponibles para el programa.

 

 



