---
title: Proporcionar información de clase
description: Proporcionar información de clase
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500125"
---
# <a name="providing-class-information"></a>Proporcionar información de clase

A menudo resulta útil para un cliente de un objeto examinar la información de tipo del objeto. Dado el CLSID del objeto, un cliente puede buscar la biblioteca de tipos del objeto mediante entradas del Registro y, a continuación, puede examinar la biblioteca de tipos en busca de la entrada de la coclase en la biblioteca que coincida con el CLSID.

Sin embargo, no todos los objetos tienen un CLSID, aunque todavía necesitan proporcionar información de tipo. Además, es conveniente que un cliente tenga una manera de simplemente pedir a un objeto su información de tipo en lugar de pasar por todo el tedium para extraer la misma información de las entradas del Registro. Esta funcionalidad es importante cuando se trabaja con interfaces salientes en objetos conectables. (Consulte [Uso de IProvideClassInfo](using-iprovideclassinfo.md) para obtener más información sobre cómo los objetos conectables proporcionan esta funcionalidad).

En estos casos, un cliente puede consultar el objeto [**para IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Si existen estas interfaces, el cliente llama al [**método GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) para obtener la información de tipo de la interfaz.

Al implementar [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2,**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)un objeto especifica que puede proporcionar información de tipo para toda su clase; es decir, lo que describiría en su sección de la coclase de su biblioteca de tipos, si tiene una. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) devuelve un **puntero ITypeInfo** correspondiente a la información de la coclase del objeto. A través **de este puntero ITypeInfo,** el cliente puede examinar todas las definiciones de interfaz entrante y saliente del objeto.

El objeto también puede proporcionar [**IProvideClassInfo2.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) La **interfaz IProvideClassInfo2** es una extensión sencilla de [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) que facilita la recuperación rápida y sencilla de los identificadores de interfaz saliente de un objeto para su conjunto de eventos predeterminado. **IProvideClassInfo2** se deriva de **IProvideClassInfo**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




