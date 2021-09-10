---
title: Implementación de IClassFactory
description: Implementación de IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369515"
---
# <a name="implementing-iclassfactory"></a>Implementación de IClassFactory

Cuando un cliente usa un CLSID para solicitar la creación de una instancia de objeto, el primer paso es la creación de un objeto de clase, un objeto intermedio que contiene una implementación de los métodos de la [**interfaz IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) Aunque COM proporciona varias funciones de creación de instancias, el primer paso en la implementación de estas funciones es la creación de un objeto de clase.

Como resultado, todos los servidores deben implementar los métodos de la [**interfaz IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) que contiene dos métodos:

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Este método debe crear una instancia sin inicializar del objeto y devolver un puntero a una interfaz solicitada en el objeto .
-   [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Este método simplemente incrementa el recuento de referencias en el objeto de clase para asegurarse de que el servidor permanece en memoria y no se apaga antes de que el cliente esté listo para que lo haga.

Para permitir que un servidor sea responsable de su propia licencia, COM define [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), que hereda su definición de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Por lo tanto, un servidor que **implementa IClassFactory2** debe, por definición, implementar los métodos de **IClassFactory**.

COM también proporciona funciones auxiliares para implementar servidores fuera de proceso. Para obtener más información, vea [Asistentes de implementación](out-of-process-server-implementation-helpers.md)de servidor fuera de proceso .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> <dt>

[Licencias e IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 