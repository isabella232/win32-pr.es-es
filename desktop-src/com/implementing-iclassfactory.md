---
title: Implementación de IClassFactory
description: Implementación de IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421441"
---
# <a name="implementing-iclassfactory"></a>Implementación de IClassFactory

Cuando un cliente usa un CLSID para solicitar la creación de una instancia de objeto, el primer paso es la creación de un objeto de clase, un objeto intermedio que contiene una implementación de los métodos de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Aunque COM proporciona varias funciones de creación de instancias, el primer paso en la implementación de estas funciones es la creación de un objeto de clase.

Como resultado, todos los servidores deben implementar los métodos de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , que contiene dos métodos:

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Este método debe crear una instancia no inicializada del objeto y devolver un puntero a una interfaz solicitada en el objeto.
-   [**Lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Este método solo incrementa el recuento de referencias en el objeto de clase para asegurarse de que el servidor permanece en la memoria y no se apaga antes de que el cliente esté listo para que lo haga.

Para permitir que un servidor sea responsable de sus propias licencias, COM define [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), que hereda su definición de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Por lo tanto, un servidor que implementa **IClassFactory2** debe implementar los métodos de **IClassFactory**, por definición.

COM también proporciona funciones auxiliares para implementar servidores fuera de proceso. Para obtener más información, vea [aplicaciones auxiliares de implementación de servidor fuera de proceso](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> <dt>

[Licencias y IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 