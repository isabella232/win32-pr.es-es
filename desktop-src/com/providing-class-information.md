---
title: Proporcionar información de clase
description: Proporcionar información de clase
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148802"
---
# <a name="providing-class-information"></a>Proporcionar información de clase

A menudo resulta útil que un cliente de un objeto examine la información de tipo del objeto. Dado el CLSID del objeto, un cliente puede localizar la biblioteca de tipos del objeto mediante las entradas del registro y, a continuación, puede examinar la biblioteca de tipos para la entrada de coclase en la biblioteca que coincide con el CLSID.

Sin embargo, no todos los objetos tienen un CLSID, aunque todavía necesitan proporcionar información de tipo. Además, es conveniente que un cliente tenga una manera de solicitar simplemente un objeto para su información de tipo en lugar de pasar por todos los tediosas tareas para extraer la misma información de las entradas del registro. Esta capacidad es importante cuando se trabaja con interfaces de salida en objetos conectables. (Consulte [uso de IProvideClassInfo](using-iprovideclassinfo.md) para obtener más información sobre cómo los objetos conectables proporcionan esta capacidad).

En estos casos, un cliente puede consultar el objeto para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Si existen estas interfaces, el cliente llama al método [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) para obtener la información de tipo de la interfaz.

Mediante la implementación de [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un objeto especifica que puede proporcionar información de tipo para toda la clase; es decir, lo que describiría en su sección coclass de su biblioteca de tipos, si tiene uno. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) devuelve un puntero **ITypeInfo** que corresponde a la información de coclase del objeto. A través de este puntero **ITypeInfo** , el cliente puede examinar todas las definiciones de interfaz de entrada y de salida del objeto.

El objeto también puede proporcionar [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). La interfaz **IProvideClassInfo2** es una extensión simple para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) que facilita y agiliza la recuperación de los identificadores de interfaz de salida de un objeto para su conjunto de eventos predeterminado. **IProvideClassInfo2** se deriva de **IProvideClassInfo**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




