---
title: Atributos de alias y serialización
description: Las aplicaciones distribuidas casi siempre pasan datos entre programas de cliente y servidor cuando llaman a procedimientos de interfaz.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- MIDL de IDL, atributos MIDL, alias y serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159689"
---
# <a name="aliasing-and-marshaling-attributes"></a>Atributos de alias y serialización

Las aplicaciones distribuidas casi siempre pasan datos entre programas de cliente y servidor cuando llaman a procedimientos de interfaz. Los desarrolladores usan MIDL para describir los datos que los programas de cliente y servidor pasan de forma estándar. El compilador MIDL crea programas de código auxiliar de aplicación, o proxy, para el cliente y el servidor que convierten los datos en un formato estandarizado que se puede enviar a través de una red. Este formato, el formato de representación de datos de red ( JPEG), a menudo se denomina formato de conexión de los datos. Los códigos auxiliares deben convertir los datos de su formato nativo en el espacio de memoria del programa a CONVERT. Esta conversión se denomina serialización de los datos. Cuando un programa cliente o servidor recibe datos, debe convertir los datos de CONVERT al formato nativo de ese programa. Esto se denomina desmarque de los datos.

Use los atributos de alias y serialización para controlar cómo se empaquetan los datos en formato JPEG y se transmiten a través de la red.



| Atributo                             | Uso                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**llamar \_ a como**](call-as.md)           | Mapas una función no remotable a una llamada a procedimiento remoto.                                                                      |
| [**iid \_ es**](iid-is.md)             | Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.                                     |
| [**transmitir \_ como**](transmit-as.md)   | Convierte un tipo de datos en un tipo más sencillo para la transmisión a través de una red.                                                       |
| [**wire \_ marshal**](wire-marshal.md) | Similar a [**transmitir \_ como**](transmit-as.md) , pero implementa las rutinas para cambiar el tamaño, serializar, desmarshal y liberar los datos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión de tipos y serialización de atributos ACF](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




