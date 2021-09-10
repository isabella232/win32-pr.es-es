---
title: Uso de IProvideClassInfo
description: Uso de IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369796"
---
# <a name="using-iprovideclassinfo"></a>Uso de IProvideClassInfo

Un objeto conectable puede ofrecer las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que sus clientes puedan examinar fácilmente su información de tipo. Esta funcionalidad es importante cuando se trabaja con interfaces salientes, que, por definición, se definen mediante un objeto pero que un cliente implementa en su propio objeto receptor. En algunos casos, una interfaz saliente se conoce en tiempo de compilación para el objeto conectable y el objeto receptor; este es el caso de [**IPropertyNotifySink.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)

Sin embargo, en otros casos, solo el objeto conectable conoce sus definiciones de interfaz salientes en tiempo de compilación. En estos casos, el cliente debe obtener la información de tipo de la interfaz saliente para que pueda proporcionar dinámicamente un receptor que admita los puntos de entrada correctos, como se indica a continuación:

1.  El cliente enumera los puntos de conexión y, a continuación, para obtener los IID de las interfaces salientes compatibles con el objeto conectable, llama a [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada punto de conexión.
2.  El cliente consulta el objeto conectable para una de las interfaces [**IProvideClassInfo.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)
3.  El cliente llama a los métodos de las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obtener la información de tipo de la interfaz saliente.
4.  El cliente crea un objeto receptor que admite la interfaz saliente.
5.  El proceso continúa y el cliente llama a [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar su receptor al punto de conexión.

En la información de tipo, el origen [**del**](/windows/desktop/Midl/source) atributo marca una [**interfaz**](/windows/desktop/Midl/interface) o [**dispinterface**](/windows/desktop/Midl/dispinterface) enumerada en una [**coclase**](/windows/desktop/Midl/coclass) como una interfaz saliente. Las enumeradas sin este atributo se consideran interfaces entrantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de objetos conectables](connectable-object-interfaces.md)
</dt> <dt>

[Proporcionar información de clase](providing-class-information.md)
</dt> </dl>

 

 