---
title: Responsabilidades del servidor COM
description: Responsabilidades del servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369444"
---
# <a name="com-server-responsibilities"></a>Responsabilidades del servidor COM

Una de las formas más importantes para que un cliente obtenga un puntero a un objeto es que el cliente pida que se inicia un servidor y que se cree y active una instancia del objeto proporcionado por el servidor. Es responsabilidad del servidor asegurarse de que esto sucede correctamente. Hay varias partes importantes en esto.

El servidor debe implementar código para un objeto de clase mediante una implementación de la [**interfaz IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2.**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

El servidor debe registrar su CLSID en el registro del sistema en la máquina en la que reside y, además, tiene la opción de publicar su ubicación de máquina en otros sistemas de una red para permitir que los clientes lo llamen sin necesidad de que el cliente conozca la ubicación del servidor.

El servidor es responsable principalmente de la seguridad; es decir, en su mayor parte, el servidor determina si proporcionará un puntero a uno de sus objetos a un cliente.

Los servidores en proceso deben implementar y exportar determinadas funciones que permiten al proceso de cliente crear instancias de ellas.

En los temas siguientes se detallan las responsabilidades del servidor COM:

-   [Implementación de IClassFactory](implementing-iclassfactory.md)
-   [Licencias e IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registro de servidores COM](registering-com-servers.md)
-   [Asistentes de implementación del servidor fuera de proceso](out-of-process-server-implementation-helpers.md)
-   [Creación y optimizaciones de GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 