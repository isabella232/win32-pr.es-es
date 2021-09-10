---
title: Apertura y cierre Secuencias
description: Apertura y cierre Secuencias
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Función AVIFileGetStream
- Función AVIStreamRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372434"
---
# <a name="opening-and-closing-streams"></a>Apertura y cierre Secuencias

La apertura de flujos de datos es similar a la apertura de archivos. Puede abrir una secuencia mediante la [**función AVIFileGetStream.**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) Esta función crea una interfaz de secuencia, coloca un identificador de la secuencia en la interfaz y devuelve un puntero a la interfaz . **AVIFileGetStream también** mantiene un recuento de referencias de las aplicaciones que han abierto una secuencia, pero no de las que la han cerrado.

Si desea acceder a una única secuencia de un archivo, puede abrir el archivo y la secuencia mediante la [**función AVIStreamOpenFromFile.**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) Esta función combina las operaciones y los argumentos de función de las [**funciones AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **y AVIFileGetStream.**

Para tener acceso a más de una secuencia de un archivo, use **AVIFileOpen** una vez seguido de varias llamadas a **AVIFileGetStream.**

Puede incrementar el recuento de referencias de una secuencia mediante la [**función AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) para mantener abierta una secuencia cuando se usa una función que normalmente cerraría la secuencia.

Puede cerrar una secuencia mediante la [**función AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) Esta función disminuye el recuento de referencias de la secuencia y la cierra cuando el recuento de referencias alcanza cero. Las aplicaciones deben equilibrar el recuento de referencias incluyendo una llamada a **AVIStreamRelease** para cada uso de las funciones [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** o **AVIStreamOpenFromFile.** Cuando se libera una secuencia que se ha abierto mediante **AVIStreamOpenFromFile,** AVIFile cierra el archivo que contiene la secuencia. Si la aplicación publica un archivo que tiene flujos de datos abiertos, AVIFile no cerrará las secuencias hasta que se liberen todas las secuencias.

 

 




