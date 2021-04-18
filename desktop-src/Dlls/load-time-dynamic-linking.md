---
description: Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información del enlazador colocada en el archivo para buscar los nombres de los archivos dll utilizados por el proceso.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Vinculación dinámica Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546710"
---
# <a name="load-time-dynamic-linking"></a>Vinculación dinámica Load-Time

Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información del enlazador colocada en el archivo para buscar los nombres de los archivos dll utilizados por el proceso. Después, el sistema busca los archivos dll. Para obtener más información, vea [orden de búsqueda en la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md).

Si el sistema no encuentra un archivo DLL necesario, finaliza el proceso y muestra un cuadro de diálogo que informa del error al usuario. De lo contrario, el sistema asigna el archivo DLL en el espacio de direcciones virtuales del proceso e incrementa el recuento de referencias de DLL.

El sistema llama a la función de punto de entrada. La función recibe un código que indica que el proceso está cargando el archivo DLL. Si la función de punto de entrada no devuelve el valor TRUE, el sistema finalizará el proceso y notificará un error. Para obtener más información sobre la función de punto de entrada, vea [biblioteca de vínculos dinámicos Entry-Point función](dynamic-link-library-entry-point-function.md).

Por último, el sistema modifica la tabla de direcciones de función con las direcciones de inicio de las funciones DLL importadas.

El archivo DLL se asigna en el espacio de direcciones virtuales del proceso durante su inicialización y se carga en la memoria física solo cuando sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Load-Time vinculación dinámica](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



