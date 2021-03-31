---
description: Un proceso utiliza la función CreateFile para abrir un identificador de un recurso de comunicaciones.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Identificadores de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423355"
---
# <a name="communications-resource-handles"></a>Identificadores de recursos de comunicaciones

Un proceso utiliza la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador de un recurso de comunicaciones. Por ejemplo, si se especifica COM1, se abre un identificador de un puerto serie y LPT1 se abre un identificador a un puerto paralelo. Si otro proceso está usando actualmente el recurso especificado, se produce un error en **CreateFile** . Cualquier subproceso del proceso puede utilizar el identificador devuelto por **CreateFile** para identificar el recurso en cualquiera de las funciones que tienen acceso al recurso.

Cuando el proceso llama a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, especifica los siguientes atributos:

-   El tipo de acceso de lectura y escritura para el recurso especificado.
-   Si los procesos secundarios pueden heredar el identificador.
-   Si el identificador se puede usar en operaciones de e/s superpuestas (asincrónicas). (Para obtener una descripción de las operaciones superpuestas, vea [Synchronization](/windows/desktop/Sync/synchronization)).

Cuando el proceso utiliza [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, debe especificar ciertos valores para los parámetros siguientes:

-   El parámetro *fdwShareMode* debe ser cero y abrir el recurso para el acceso exclusivo.
-   El parámetro *fdwCreate* debe especificar la \_ marca existente abrir.
-   El parámetro *hTemplateFile* debe ser **null**.

Al usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un controlador directamente en un dispositivo, una aplicación debe usar los caracteres especiales " \\ \\ . \\ " para identificar el dispositivo. Por ejemplo, para abrir un identificador de la unidad a, especifique \\ \\ . \\ r: para el parámetro *lpszName* de **CreateFile**. El proceso de llamada puede usar el identificador de la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar códigos de control al dispositivo.

 

 
