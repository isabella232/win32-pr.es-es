---
title: Paquete de administración de memoria RpcSs
description: El par de asignador predeterminado/desasignador usado por el código auxiliar y el tiempo de ejecución cuando la asignación de memoria en nombre de la aplicación es el usuario de MIDL de \_ asignación de usuarios \_ o de MIDL \_ \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488111"
---
# <a name="rpcss-memory-management-package"></a>Paquete de administración de memoria RpcSs

El par de asignador predeterminado/desasignador utilizado por el código auxiliar y el tiempo de ejecución al asignar memoria en nombre de la aplicación es el **usuario de MIDL que \_ \_ asigna** el usuario de / **MIDL \_ \_ gratis**. Sin embargo, puede elegir el paquete RpcSs en lugar del valor predeterminado mediante el atributo ACF de **\[ habilitar \_ asignación \]**. El paquete RpcSs consta de funciones RPC que comienzan con el prefijo **RPCSS** o **RpcSm**. El paquete RpcSs no se recomienda para las aplicaciones Windows.

> [!Note]  
> El paquete de administración de memoria RPCSS está obsoleto. Se recomienda usar en su lugar la [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y el [**\_ usuario \_ de MIDL**](/windows/desktop/Midl/midl-user-free-1) .

 

En el modo **/OSF** , el paquete RPCSS está habilitado automáticamente para los códigos auxiliares generados por MIDL cuando se usan punteros completos, cuando los argumentos requieren la asignación de memoria o como resultado de usar el atributo **\[ enable \_ allocate \]** . En el modo predeterminado (Microsoft Extended), el paquete RpcSs solo está habilitado cuando se usa el atributo **\[ enable \_ allocate \]** . El atributo **\[ enable \_ allocate \]** habilita el entorno RPCSS mediante el código auxiliar del lado servidor. El lado cliente se alerta a la posibilidad de que se pueda habilitar el paquete RpcSs. En el modo **/OSF** , el lado cliente no se ve afectado.

Cuando el paquete RpcSs está habilitado, la asignación de memoria en el servidor se logra con el par de asignador y desasignador de administración de memoria RpcSs privado. Puede asignar memoria mediante el mismo mecanismo llamando a [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Al volver del código auxiliar del servidor, se libera automáticamente toda la memoria asignada por el paquete RpcSs. En el ejemplo siguiente se muestra cómo habilitar el paquete RpcSs:

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

La aplicación puede liberar explícitamente la memoria mediante la invocación de la función [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) . Tenga en cuenta que estas funciones no liberan memoria realmente. Lo marcan para su eliminación. La biblioteca RPC libera la memoria cuando el programa llama a [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

También puede habilitar el entorno de administración de memoria para la aplicación mediante una llamada a la rutina [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (y puede deshabilitarla mediante una llamada a la rutina [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ). Una vez habilitado, el código de aplicación puede asignar y desasignar memoria llamando a las funciones del paquete RpcSs.

 

 