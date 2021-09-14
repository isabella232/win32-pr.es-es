---
title: Generar información de error
description: Si un servidor o una aplicación encuentra un error irrevocado mientras se llama a través de RPC, debe indicar al tiempo de ejecución de RPC que se ha producido un error y, idealmente, debe agregar información sobre el error para facilitar la solución de problemas.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259780"
---
# <a name="generating-error-information"></a>Generar información de error

Si un servidor o una aplicación encuentra un error irrevocado mientras se llama a través de RPC, debe indicar al tiempo de ejecución de RPC que se ha producido un error y, idealmente, debe agregar información sobre el error para facilitar la solución de problemas.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Indicación de errores irreales en el tiempo de ejecución de RPC

Para indicar un error en el tiempo de ejecución de RPC, llame a la función [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) mientras se encuentra en el subproceso RPC en el que se llamó a la excepción, o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) si procesa la llamada de forma asincrónica en otro subproceso. Devolver un código de error de la rutina de servidor, como la rutina de administrador, no es suficiente: según la especificación RPC, el valor devuelto de la función no tiene semántica de errores en el servidor, independientemente de la configuración del archivo idl/acf.

Cuando se produzca un error grave en el componente, realice cualquier limpieza que considere necesaria y, a continuación, llame a la [**función RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) con el código de error. La única diferencia entre **RpcRaiseException** y devolver un código de error es cuando se llama a **RpcRaiseException,** no se serializan los parámetros out. Esto suele ser una ventaja, ya que evitar parámetros no inicializados resulta innecesario.

## <a name="generating-additional-extended-error-information"></a>Generación de información de error extendida adicional

Al igual que el tiempo de ejecución rpc crea una cadena de registros de error, el servidor o la aplicación pueden agregar sus propios registros a la cadena. Este enfoque suele ayudar en el proceso de solución de problemas. Por ejemplo, un servidor puede intentar abrir un archivo determinado y recibir un error de archivo no encontrado. Simplemente devolver el error 2 no sería útil para determinar qué archivo falta.

En su lugar, el servidor podría llamar a la [**función RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) y proporcionar un parámetro de cadena, ANSI o Unicode, en el registro de error que indica la ruta de acceso completa del archivo que estaba buscando. Cuando toda esta información aparece en la pantalla del usuario en un equipo remoto, la solución de problemas se vuelve trivial. Se puede realizar una comprobación simple de si el archivo existe, especialmente porque el tiempo de ejecución rpc ya proporciona el nombre del equipo en cuestión.

La [**llamada a la función RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) puede producir un error si no hay suficiente memoria disponible, aunque solo requiera unos pocos bytes de espacio en el montón. Además, los registros agregados por **RpcErrorAddRecord se** acumulan en un subproceso determinado. Normalmente, el tiempo de ejecución limpia esos registros antes de llamar a la rutina del servidor, pero si se usa información de error extendida fuera de RPC, se encarga de limpiar el error extendido acumulado en el subproceso mediante una llamada a [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).

 

 




