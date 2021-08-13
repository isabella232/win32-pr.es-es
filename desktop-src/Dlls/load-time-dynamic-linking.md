---
description: Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información que el vinculador coloca en el archivo para buscar los nombres de los archivos DLL que usa el proceso.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time dynamic linking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0adac32841d822bba67031dd79171c52f25d8308b055aee2c55bb804ebefe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649363"
---
# <a name="load-time-dynamic-linking"></a>Load-Time dynamic linking

Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información que el vinculador coloca en el archivo para buscar los nombres de los archivos DLL que usa el proceso. A continuación, el sistema busca los archivos DLL. Para obtener más información, vea [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

Si el sistema no encuentra un archivo DLL necesario, finaliza el proceso y muestra un cuadro de diálogo que informa del error al usuario. De lo contrario, el sistema asigna el archivo DLL al espacio de direcciones virtuales del proceso e incrementa el recuento de referencias de DLL.

El sistema llama a la función de punto de entrada. La función recibe un código que indica que el proceso está cargando el archivo DLL. Si la función de punto de entrada no devuelve el valor TRUE, el sistema finalizará el proceso y notificará un error. Para obtener más información sobre la función de punto de entrada, vea [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Por último, el sistema modifica la tabla de direcciones de función con las direcciones iniciales de las funciones DLL importadas.

El archivo DLL se asigna al espacio de direcciones virtuales del proceso durante su inicialización y se carga en la memoria física solo cuando sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso Load-Time dynamic linking](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



