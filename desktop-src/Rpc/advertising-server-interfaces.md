---
title: Interfaces de servidor de publicidad
description: El lado del servidor de una aplicación que usa identificadores automáticos debe llamar a la función RpcNsBindingExport para que la información de enlace del servidor esté disponible para los clientes.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075769"
---
# <a name="advertising-server-interfaces"></a>Interfaces de servidor de publicidad

El lado del servidor de una aplicación que usa identificadores automáticos debe llamar a la función [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para que la información de enlace del servidor esté disponible para los clientes. Los identificadores de enlace automáticos requieren un servicio de nombres que se ejecute en un servidor al que pueda acceder el cliente. La implementación de Microsoft del servicio de nombres, localizador de Microsoft, administra los identificadores automáticos. Las aplicaciones de servidor que usan identificadores de enlace implícitos y explícitos también pueden anunciar su presencia en la base de datos del servicio de nombres.

Normalmente, el servidor llama a las siguientes funciones en tiempo de ejecución:

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

Las llamadas a las dos primeras funciones de este fragmento de código son similares al [ejemplo Hello, World](tutorial.md). Estas funciones realizan información sobre el enlace disponible para el cliente. Las llamadas a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) y [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) colocan la información en la base de datos del servicio de nombres. La llamada a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) rellena el vector de enlace con identificadores de enlace válidos antes de que los identificadores se exporten al servicio de nombres. Una vez que el programa de servidor exporta los identificadores a la base de datos, el cliente (o los códigos auxiliares de cliente) puede llamar a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) y [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener esta información. Para obtener más información, consulte [búsqueda de sistemas host de servidor](finding-server-host-systems.md).

Las llamadas a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) y [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) y sus estructuras de datos asociadas tienen un aspecto similar al siguiente:

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

Tenga en cuenta que el parámetro [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* es un puntero a un puntero a un [**\_ \_ Vector de enlace RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Recuerde también que cada llamada a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) debe ir seguida de una llamada a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Para quitar la interfaz exportada de la base de datos del servicio de nombres, el servidor llama a [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) como se muestra a continuación:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

La función [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) solo debe usarse cuando el servicio se quita permanentemente. No debe usarse cuando el servicio está deshabilitado temporalmente, como cuando se apaga el servidor para el mantenimiento. Un programa de servidor puede registrarse en la base de datos del servicio de nombres, pero no estar disponible porque el servidor está sin conexión temporalmente. La aplicación cliente debe contener el código de control de excepciones para esta condición.

Para obtener más información sobre el contenido y el formato de la base de datos del servicio de nombres, vea [la base de datos del servicio de nombres RPC](the-rpc-name-service-database.md).

Las aplicaciones pueden utilizar el servicio Active Directory si los programas cliente y servidor se ejecutan en Windows 2000. Los equipos que ejecutan los programas de cliente y servidor de deben ser miembros de un dominio de Windows 2000.

Para anunciar su presencia mediante el servicio Active Directory, el programa de servidor debe ejecutarse en el contexto de seguridad de un administrador de dominio. Si se ejecuta en el contexto de los usuarios del dominio, un administrador de dominio debe modificar la lista de control de acceso (ACL) en el contenedor de servicios RPC. Para obtener más información, consulte la documentación de Active Directory.

 

 




