---
description: La vinculación dinámica presenta las siguientes ventajas con respecto a la vinculación estática.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Ventajas de la vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667633"
---
# <a name="advantages-of-dynamic-linking"></a>Ventajas de la vinculación dinámica

La vinculación dinámica presenta las siguientes ventajas con respecto a la vinculación estática:

-   Varios procesos que cargan el mismo archivo DLL en la misma dirección base comparten una única copia de la DLL en la memoria física. Esto ahorra memoria del sistema y reduce el intercambio.
-   Cuando cambian las funciones de un archivo DLL, no es necesario volver a compilar o volver a vincular las aplicaciones que las usan, siempre y cuando no cambien los argumentos de la función, las convenciones de llamada y los valores devueltos. En cambio, el código de un objeto vinculado estáticamente requiere que se vuelva a vincular la aplicación cuando cambien las funciones.
-   Un archivo DLL puede proporcionar soporte técnico después del mercado. Por ejemplo, se puede modificar una DLL de controlador de pantalla para que admita una pantalla que no estaba disponible cuando la aplicación se envió inicialmente.
-   Los programas escritos en lenguajes de programación diferentes pueden llamar a la misma función DLL siempre que los programas sigan la misma Convención de llamada que usa la función. La Convención de llamada (como C, Pascal o llamada estándar) controla el orden en el que la función de llamada debe introducir los argumentos en la pila, tanto si la función como la función de llamada es responsable de limpiar la pila y de si se pasan argumentos en los registros. Para obtener más información, vea la documentación que se incluye con el compilador.

Una posible desventaja de utilizar archivos DLL es que la aplicación no es independiente; depende de la existencia de un módulo de archivo DLL separado. El sistema termina los procesos mediante la vinculación dinámica en tiempo de carga si requieren un archivo DLL que no se encuentra en el inicio del proceso y proporciona un mensaje de error al usuario. El sistema no finaliza un proceso que usa la vinculación dinámica en tiempo de ejecución en esta situación, pero las funciones exportadas por el archivo DLL que faltan no están disponibles para el programa.

 

 



