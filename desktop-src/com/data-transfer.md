---
title: Transferencia de datos
description: Transferencia de datos
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98e7f546cab245e1f2d2d06036379ea5b28526edcf42aa8a364ea04688db034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993495"
---
# <a name="data-transfer"></a>Transferencia de datos

El modelo de objetos componentes (COM) proporciona un mecanismo estándar para transferir datos entre aplicaciones. Este mecanismo es el *objeto de datos*, que es simplemente cualquier objeto COM que implementa la interfaz [**IDataObject.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Algunos objetos de datos, como un fragmento de texto copiado en el Portapapeles, tienen **IDataObject** como única interfaz. Otros, como los objetos de documento compuestos, exponen varias interfaces, de las cuales **IDataObject** es simplemente una. Los objetos de datos son fundamentales para el funcionamiento de documentos compuestos, aunque también tienen una aplicación generalizada fuera de esa tecnología OLE.

Al intercambiar punteros a un objeto de datos, los proveedores y consumidores de datos pueden administrar las transferencias de datos de forma uniforme, independientemente del formato de los datos, el tipo de medio utilizado para transferir los datos o el dispositivo de destino en el que se representarán. Puede incluir compatibilidad en la aplicación para transferencias básicas del Portapapeles, transferencias de arrastrar y colocar y transferencias de documentos compuestos OLE con una única implementación de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Una vez hecho esto, la cantidad de código necesario para adaptarse a la semántica especial de cada protocolo es mínima.

Para obtener más información, vea los temas siguientes:

-   [Interfaces de transferencia de datos](data-transfer-interfaces.md)
-   [Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
-   [Arrastrar y colocar](drag-and-drop.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




