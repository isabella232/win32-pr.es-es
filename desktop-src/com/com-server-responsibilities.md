---
title: Responsabilidades del servidor COM
description: Responsabilidades del servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421461"
---
# <a name="com-server-responsibilities"></a>Responsabilidades del servidor COM

Una de las formas más importantes de que un cliente obtenga un puntero a un objeto es que el cliente pida que se inicie un servidor y que se cree y active una instancia del objeto proporcionado por el servidor. Es responsabilidad del servidor asegurarse de que esto se produce correctamente. Hay varias partes importantes para esto.

El servidor debe implementar código para un objeto de clase a través de una implementación de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .

El servidor debe registrar su CLSID en el registro del sistema en el equipo en el que reside y, además, tiene la opción de publicar su ubicación de equipo en otros sistemas de una red para que los clientes puedan llamarla sin necesidad de que el cliente conozca la ubicación del servidor.

El servidor es responsable principalmente de la seguridad; es decir, en la mayor parte, el servidor determina si proporcionará un puntero a uno de sus objetos a un cliente.

Los servidores en proceso deben implementar y exportar ciertas funciones que permiten al proceso del cliente crear instancias de ellas.

En los temas siguientes se detallan las responsabilidades del servidor COM:

-   [Implementación de IClassFactory](implementing-iclassfactory.md)
-   [Licencias y IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrar servidores COM](registering-com-servers.md)
-   [Aplicaciones auxiliares de implementación de servidor fuera de proceso](out-of-process-server-implementation-helpers.md)
-   [Creación y optimización de GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 