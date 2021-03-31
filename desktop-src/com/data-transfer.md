---
title: Transferencia de datos
description: Transferencia de datos
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532451"
---
# <a name="data-transfer"></a>Transferencia de datos

El modelo de objetos componentes (COM) proporciona un mecanismo estándar para transferir datos entre aplicaciones. Este mecanismo es el *objeto de datos*, que es simplemente cualquier objeto com que implementa la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Algunos objetos de datos, como un fragmento de texto copiado en el portapapeles, tienen **IDataObject** como su única interfaz. Otros, como los objetos de documento compuestos, exponen varias interfaces, de las cuales **IDataObject** es simplemente uno. Los objetos de datos son fundamentales para el trabajo de los documentos compuestos, aunque también tienen una aplicación generalizada fuera de esa tecnología OLE.

Al intercambiar punteros a un objeto de datos, los proveedores y consumidores de datos pueden administrar las transferencias de datos de manera uniforme, independientemente del formato de los datos, el tipo de medio utilizado para transferir los datos o el dispositivo de destino en el que se va a representar. Puede incluir compatibilidad en la aplicación para las transferencias básicas del portapapeles, las transferencias de arrastrar y colocar, y las transferencias de documentos compuestos OLE con una única implementación de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Una vez hecho esto, la cantidad de código necesaria para acomodar la semántica especial de cada protocolo es mínima.

Para obtener más información, vea los temas siguientes:

-   [Interfaces de Transferencia de datos](data-transfer-interfaces.md)
-   [Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
-   [Arrastrar y colocar](drag-and-drop.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




