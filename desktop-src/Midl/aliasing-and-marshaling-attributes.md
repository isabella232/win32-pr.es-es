---
title: Atributos de alias y serialización
description: Las aplicaciones distribuidas casi siempre pasan datos entre los programas de cliente y servidor cuando llaman a procedimientos de interfaz.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- MIDL de IDL, atributos MIDL, alias y serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076303"
---
# <a name="aliasing-and-marshaling-attributes"></a>Atributos de alias y serialización

Las aplicaciones distribuidas casi siempre pasan datos entre los programas de cliente y servidor cuando llaman a procedimientos de interfaz. Los programadores utilizan MIDL para describir los datos que los programas de cliente y servidor pasan de forma estándar. El compilador MIDL crea programas de código auxiliar de aplicación, o proxy, para el cliente y el servidor que convierte los datos en un formato normalizado que se puede enviar a través de una red. Este formato, el formato de representación de datos de red (NDR), a menudo se denomina formato de conexión de los datos. El código auxiliar debe convertir los datos de su formato nativo en el espacio de memoria del programa a NDR. Esta conversión se denomina cálculo de referencias de los datos. Cuando un cliente o un programa de servidor recibe datos, debe convertir los datos de NDR al formato nativo para ese programa. Esto se denomina anulación del cálculo de referencias de los datos.

Use atributos de alias y serialización para controlar el modo en que los datos se empaquetan en formato NDR y se transmiten a través de la red.



| Atributo                             | Uso                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**llamar a \_ como**](call-as.md)           | Asigna una función no utilizables a una llamada a procedimiento remoto.                                                                      |
| [**IID \_ es**](iid-is.md)             | Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.                                     |
| [**transmitir \_ como**](transmit-as.md)   | Convierte un tipo de datos en un tipo más simple para su transmisión a través de una red.                                                       |
| [**\_serialización de cable**](wire-marshal.md) | Similar a [**transmitir \_ como**](transmit-as.md) , pero se implementan las rutinas para ajustar el tamaño, las referencias, las referencias y la liberación de los datos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos ACF de conversión y serialización de tipos](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




