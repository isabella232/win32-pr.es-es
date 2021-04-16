---
title: Generando información de error
description: Si un servidor o aplicación encuentra un error irrecuperable mientras se llama a través de RPC, debe indicar al tiempo de ejecución de RPC que ha detectado un error y, idealmente, debe agregar información sobre el error para facilitar la solución de problemas.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676147"
---
# <a name="generating-error-information"></a>Generando información de error

Si un servidor o aplicación encuentra un error irrecuperable mientras se llama a través de RPC, debe indicar al tiempo de ejecución de RPC que ha detectado un error y, idealmente, debe agregar información sobre el error para facilitar la solución de problemas.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Que indica errores irrecuperables en el tiempo de ejecución de RPC

Para indicar un error en el tiempo de ejecución de RPC, llame a la función [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) mientras se encuentra en el SUBproceso RPC en el que se llamó a la excepción, o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) si procesa la llamada de forma asincrónica en otro subproceso. Devolver un código de error de la rutina del servidor, como la rutina Manager, no es suficiente, de acuerdo con la especificación RPC, el valor devuelto de la función no tiene ninguna semántica de error en el servidor, independientemente de la configuración del archivo IDL/ACF.

Cuando se produce un error irrecuperable en el componente, realice cualquier limpieza que considere necesaria y, a continuación, llame a la función [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) con el código de error. La única diferencia entre **RpcRaiseException** y la devolución de un código de error es cuando se llama a **RpcRaiseException** , no se calculan las referencias de los parámetros out. Esto suele ser una ventaja, ya que evitar los parámetros out no inicializados deja de ser necesario.

## <a name="generating-additional-extended-error-information"></a>Generando información adicional de errores extendidos

Del mismo modo que el tiempo de ejecución de RPC genera una cadena de registros de error, el servidor o la aplicación pueden agregar sus propios registros a la cadena. Este enfoque suele ayudarle en el proceso de solución de problemas. Por ejemplo, un servidor puede intentar abrir un archivo determinado y recibir un error de archivo no encontrado. Simplemente devolver el error 2 no sería útil para determinar qué archivo falta.

En su lugar, el servidor podría llamar a la función [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) y proporcionar un parámetro de cadena, ANSI o Unicode, en el registro de errores que indica la ruta de acceso completa del archivo que estaba buscando. Cuando toda esta información aparece en la pantalla de usuario de un equipo remoto, la solución de problemas es trivial. se puede realizar una comprobación simple de si existe el archivo, especialmente porque el nombre del equipo en cuestión ya lo proporciona el tiempo de ejecución de RPC.

La llamada a la función [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) puede producir un error si no hay suficiente memoria disponible, aunque solo requiere unos pocos bytes de espacio en el montón. Además, los registros agregados por **RpcErrorAddRecord** se acumulan en un subproceso determinado. Normalmente, el tiempo de ejecución limpia esos registros antes de llamar a la rutina del servidor, pero si la información de error extendida se usa fuera de RPC, se encarga de limpiar el error extendido acumulado en el subproceso llamando a [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).

 

 




