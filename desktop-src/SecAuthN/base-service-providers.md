---
description: Estos proveedores de servicios proporcionan las capacidades básicas de la tarjeta inteligente.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Proveedores de servicios base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002181"
---
# <a name="base-service-providers"></a>Proveedores de servicios base

Estos [*proveedores de servicios*](/windows/desktop/SecGloss/c-gly) proporcionan las capacidades básicas de la [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) . Se pueden usar para tener acceso a una única funcionalidad de tarjeta inteligente o las interfaces COM se pueden combinar para proporcionar varias funciones en un solo proveedor de servicios. Estos proveedores de servicios son los bloques de creación para desarrollar funcionalidad adicional a otros proveedores de servicios.

Las siguientes tareas pueden realizarse mediante las interfaces del proveedor de servicios base proporcionadas por el SDK de tarjeta inteligente.



| Tarea                                                                                                                   | Interfaces de proveedor de servicios base         | Archivo DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Conectarse a una tarjeta inteligente, implementar transacciones, cerrar conexiones, etc.                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| Mantener un comando APDU y [*responder APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Consultar la [*base de datos de tarjeta inteligente*](/windows/desktop/SecGloss/s-gly). | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Busque una tarjeta inteligente o un lector.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Cree una APDU de comando ISO7816-4.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Ajuste un búfer IStream mediante el uso de tipos compatibles con Visual Basic.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

En el procedimiento siguiente se muestra un uso típico de estas interfaces base del proveedor de servicios. En este ejemplo, las interfaces [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)y [**ISCardCmd**](iscardcmd.md) se usan para realizar una transacción.

**Para realizar una transacción**

1.  Cree una instancia de para todas las interfaces de proveedor de servicios base necesarias (por ejemplo, [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)y [**ISCardCmd**](iscardcmd.md)).
2.  Conéctese a una tarjeta inteligente determinada mediante los métodos de la interfaz [**ISCard**](iscard.md) .
3.  Mediante [**ISCardISO7816**](iscardiso7816.md) y un objeto [**ISCardCmd**](iscardcmd.md) , cree un comando ISO 7816-4 llamando al método **ISCardISO7816** . El comando está contenido en **ISCardCmd** como APDU del comando.
4.  Realice una transacción con la tarjeta llamando al método de transacción [**ISCard**](iscard.md) y pasando el objeto [**ISCardCmd**](iscardcmd.md) creado. Una vez completada la transacción, los resultados se almacenan en las APDU de respuesta **ISCardCmd** .
5.  Interpretar las APDU de respuesta de [**ISCardCmd**](iscardcmd.md) y repetir.
6.  Libera todas las interfaces cuando se completan las operaciones.

Para obtener información sobre el comando APDU creado en los archivos dll, vea [Building a ISO7816-4 APDU Command](building-an-iso7816-4-apdu-command.md).

 

 
