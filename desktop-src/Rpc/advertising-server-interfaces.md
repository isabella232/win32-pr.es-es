---
title: Interfaces de servidor de publicidad
description: El lado servidor de una aplicación que usa identificadores automáticos debe llamar a la función RpcNsBindingExport para que la información de enlace sobre el servidor esté disponible para los clientes.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271836"
---
# <a name="advertising-server-interfaces"></a>Interfaces de servidor de publicidad

El lado servidor de una aplicación que usa identificadores automáticos debe llamar a la función [**RpcNsBindingExport para**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) que la información de enlace sobre el servidor esté disponible para los clientes. Los identificadores de enlace automático requieren un servicio de nombres que se ejecute en un servidor al que el cliente pueda acceder. La implementación de Microsoft del servicio de nombres, Microsoft Locator, administra los identificadores automáticos. Las aplicaciones de servidor que usan identificadores de enlace implícitos y explícitos también pueden anunciar su presencia en la base de datos del servicio de nombres.

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

Las llamadas a las dos primeras funciones de este fragmento de código son similares al [ejemplo Hello, World](tutorial.md). Estas funciones hacen que la información sobre el enlace esté disponible para el cliente. Las llamadas a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) y [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ponen la información en la base de datos del servicio de nombres. La llamada a [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) rellena el vector de enlace con identificadores de enlace válidos antes de que los identificadores se exporten al servicio de nombres. Después de que el programa de servidor exporta los identificadores a la base de datos, el cliente (o códigos auxiliares de cliente) puede llamar a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) y [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener esta información. Para más información, consulte [Búsqueda de sistemas host de servidor.](finding-server-host-systems.md)

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

Tenga en cuenta [**que el parámetro RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* es un puntero a un puntero a [**RPC BINDING \_ \_ VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Recuerde también que cada llamada a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) debe ir seguida de una llamada a [**RpcBindingVectorFree.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)

Para quitar la interfaz exportada de la base de datos del servicio de nombres, el servidor llama a [**RpcNsBindingUnexport como**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) se muestra:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

La [**función RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) solo se debe usar cuando el servicio se quita permanentemente. No debe usarse cuando el servicio está deshabilitado temporalmente, por ejemplo, cuando el servidor se apaga para mantenimiento. Un programa de servidor puede registrarse con la base de datos del servicio de nombres, pero no está disponible porque el servidor está temporalmente sin conexión. La aplicación cliente debe contener código de control de excepciones para dicha condición.

Para obtener más información sobre el contenido y el formato de la base de datos del servicio de nombres, vea [The RPC Name Service Database](the-rpc-name-service-database.md).

Las aplicaciones pueden usar el Active Directory si los programas de cliente y servidor se ejecutan en Windows 2000. Los equipos que ejecutan los programas cliente y servidor deben ser miembros de un Windows 2000.

Para anunciar su presencia mediante el Active Directory, el programa de servidor debe ejecutarse en el contexto de seguridad de un administrador de dominio. Si se ejecuta en el contexto de los usuarios del dominio, un administrador de dominio debe modificar la lista de control de acceso (ACL) en el contenedor de servicios RPC. Para más información, consulte la documentación Active Directory datos.

 

 




