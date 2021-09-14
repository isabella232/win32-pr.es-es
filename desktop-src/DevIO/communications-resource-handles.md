---
description: Un proceso usa la función CreateFile para abrir un identificador en un recurso de comunicaciones.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Identificadores de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164502"
---
# <a name="communications-resource-handles"></a>Identificadores de recursos de comunicaciones

Un proceso usa la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador en un recurso de comunicaciones. Por ejemplo, si se especifica COM1, se abre un identificador en un puerto serie y LPT1 abre un identificador en un puerto paralelo. Si otro proceso está utilizando actualmente el recurso especificado, se produce un error **en CreateFile.** Cualquier subproceso del proceso puede usar el identificador devuelto por **CreateFile** para identificar el recurso en cualquiera de las funciones que acceden al recurso.

Cuando el proceso llama a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, especifica los atributos siguientes:

-   Qué tipo de acceso de lectura y escritura existe para el recurso especificado.
-   Si los procesos secundarios pueden heredar el identificador.
-   Si el identificador se puede usar en operaciones de E/S superpuestas (asincrónicas). (Para obtener una descripción de las operaciones superpuestas, vea [Sincronización).](/windows/desktop/Sync/synchronization)

Cuando el proceso usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, debe especificar determinados valores para los parámetros siguientes:

-   El *parámetro fdwShareMode* debe ser cero, lo que abre el recurso para el acceso exclusivo.
-   El *parámetro fdwCreate* debe especificar la marca OPEN \_ EXISTING.
-   El *parámetro hTemplateFile* debe ser **NULL.**

Cuando se [**usa CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador directamente en un dispositivo, una aplicación debe usar los caracteres especiales " \\ \\ . " para identificar \\ el dispositivo. Por ejemplo, para abrir un identificador para la unidad A, especifique \\ \\ . \\ a: para el *parámetro lpszName* de **CreateFile**. El proceso de llamada puede usar el identificador de la [**función DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar códigos de control al dispositivo.

 

 
