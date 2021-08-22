---
title: Evitar varias cargas
description: Al cargar un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente bits y el servidor BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c08555acf8bcdc99576675b0ec5852f322f7b37fea9821f3f0156352a29b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701705"
---
# <a name="preventing-multiple-uploads"></a>Evitar varias cargas

Al cargar un archivo, BITS crea un identificador de sesión que identifica la sesión de carga en el cliente bits y el servidor BITS. Si la conexión entre el cliente bits y el servidor se ha roto mientras BITS carga un archivo, el cliente usará el identificador de sesión para intentar reanudar la carga.

Si el cliente bits se conecta al mismo servidor que antes, el servidor reconocerá el identificador de sesión y la carga se reanudará desde el punto de interrupción. Sin embargo, si el cliente se conecta a un servidor diferente, el cliente debe iniciar la carga desde el principio porque el nuevo servidor no tiene el contexto de sesión ni los datos cargados previamente. BITS puede conectarse a un servidor diferente cuando el servidor BITS se hospeda en una granja de servidores web y la propiedad de extensión DE IIS bits, [BITSHostId](bits-iis-extension-properties.md), no está establecida. La propiedad BITSHostId impide los reinicios al forzar al cliente bits a conectarse a la dirección única del servidor anterior en lugar de a la dirección del servidor compartido.

El servidor BITS intentará enviar el archivo de carga solo una vez a la aplicación de servidor, pero es posible que el archivo se envíe más de una vez. Esto puede ocurrir, por ejemplo, si el servidor BITS envía el archivo a la aplicación de servidor y, a continuación, finaliza mientras espera la respuesta de la aplicación de servidor. El cliente bits recibirá un código de error de la capa HTTP y volverá a intentar la carga después de un retraso. Si el servidor permanece sin conexión durante más tiempo que el tiempo de espera [de BITSHostIdFallbackTimeout,](bits-iis-extension-properties.md) el cliente finalmente enviará la solicitud a la dirección del servidor compartido de nuevo. un servidor BITS diferente recibirá el archivo y lo volverá a entregar a la aplicación de servidor.

Puede producirse un caso similar incluso con un único servidor front-end. Por ejemplo, cuando el cliente ha cargado todo el archivo en el servidor, el bloque final hace que el servidor reenvía el archivo a la aplicación de servidor. Si el servidor BITS o la aplicación de servidor finalizan después de procesar el archivo, pero antes de enviar la confirmación al cliente, el cliente recibirá un código de error y lo volverá a intentar más adelante. Cuando el cliente vuelva a intentarlo, el servidor BITS verá que se ha cargado el bloque final y reenviará de nuevo el archivo a la aplicación de servidor. Si recibir el archivo de carga varias veces es un problema para la aplicación de servidor, considere la posibilidad de incluir un identificador de transacción en los datos.

 

 




