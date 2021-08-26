---
title: Paquete de administración de memoria rpcSs
description: El par de asignador/desasignador predeterminado utilizado por los códigos auxiliares y el tiempo de ejecución al asignar memoria en nombre de la aplicación es midl \_ user \_ allocate/midl \_ user \_ free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93648b56ed47eb98a83b27a39b606fa2a51de9bf5791ad1b732e7169ef5dfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018185"
---
# <a name="rpcss-memory-management-package"></a>Paquete de administración de memoria rpcSs

El par de asignador/desasignador predeterminado utilizado por los códigos auxiliares y el tiempo de ejecución al asignar memoria en nombre de la aplicación es **midl \_ user \_ allocate** / **midl user \_ \_ free**. Sin embargo, puede elegir el paquete RpcSs en lugar del valor predeterminado mediante el atributo ACF **\[ enable \_ allocate \]**. El paquete RpcSs consta de funciones RPC que comienzan con el prefijo **RpcSs** **o RpcSm**. No se recomienda el paquete RpcSs para Windows aplicaciones.

> [!Note]  
> El paquete de administración de memoria rpcss está obsoleto. Se recomienda que se [**utilicen midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) y [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1) en su lugar.

 

En el modo **/osf,** el paquete RpcSs se habilita automáticamente para los códigos auxiliares generados por MIDL cuando se usan punteros completos, cuando los argumentos requieren asignación de memoria o como resultado de usar el atributo **\[ enable \_ allocate. \]** En el modo predeterminado (extendido de Microsoft), el paquete RpcSs solo se habilita cuando se usa el atributo **\[ \_ enable allocate. \]** El **\[ atributo enable \_ allocate \]** habilita el entorno rpcSs mediante los códigos auxiliares del lado servidor. El lado cliente se alerta de la posibilidad de que el paquete RpcSs esté habilitado. En **el modo /osf,** el lado cliente no se ve afectado.

Cuando el paquete RpcSs está habilitado, la asignación de memoria en el lado servidor se realiza con el asignador de administración de memoria rpcSs privado y el par de desasignadores. Puede asignar memoria mediante el mismo mecanismo llamando a [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate).**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate) Tras la devolución del código auxiliar del servidor, se libera automáticamente toda la memoria asignada por el paquete RpcSs. En el ejemplo siguiente se muestra cómo habilitar el paquete RpcSs:

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

La aplicación puede liberar memoria explícitamente invocando la [**función RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) [**o RpcSmFree.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) Tenga en cuenta que estas funciones no liberan realmente memoria. Lo marcan para su eliminación. La biblioteca RPC libera la memoria cuando el programa llama a [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

También puede habilitar el entorno de administración de memoria para la aplicación llamando a la [**rutina RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (y puede deshabilitarlo llamando a la [**rutina RpcSmDisableAllocate).**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) Una vez habilitado, el código de la aplicación puede asignar y desasignar memoria llamando a funciones desde el paquete RpcSs.

 

 