---
title: Usar IProvideClassInfo
description: Usar IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078441"
---
# <a name="using-iprovideclassinfo"></a>Usar IProvideClassInfo

Un objeto conectable puede ofrecer las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) y [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que sus clientes puedan examinar fácilmente su información de tipo. Esta capacidad es importante cuando se trabaja con interfaces salientes, que, por definición, se definen mediante un objeto, pero se implementa mediante un cliente en su propio objeto receptor. En algunos casos, una interfaz de salida se conoce en tiempo de compilación para el objeto conectable y el objeto receptor. Este es el caso con [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

En otros casos, sin embargo, solo el objeto conectable conoce sus definiciones de interfaz de salida en tiempo de compilación. En estos casos, el cliente debe obtener la información de tipo de la interfaz de salida para que pueda proporcionar dinámicamente un receptor que admita los puntos de entrada correctos, como se indica a continuación:

1.  El cliente enumera los puntos de conexión y, a continuación, para obtener los IID de las interfaces salientes admitidas por el objeto conectable, llama a [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada punto de conexión.
2.  El cliente consulta el objeto conectable para una de las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .
3.  El cliente llama a los métodos de las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obtener la información de tipo de la interfaz de salida.
4.  El cliente crea un objeto receptor que admite la interfaz de salida.
5.  El proceso continúa y el cliente llama a [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar su receptor al punto de conexión.

En la información de tipo, el [**origen**](/windows/desktop/Midl/source) del atributo marca una [**interfaz**](/windows/desktop/Midl/interface) o [**dispinterface**](/windows/desktop/Midl/dispinterface) que aparece bajo una [**coclase**](/windows/desktop/Midl/coclass) como una interfaz de salida. Los que aparecen sin este atributo se consideran interfaces entrantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objeto conectables](connectable-object-interfaces.md)
</dt> <dt>

[Proporcionar información de clase](providing-class-information.md)
</dt> </dl>

 

 