---
description: Estos proveedores de servicios proporcionan las funcionalidades básicas de tarjeta inteligente.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Proveedores de servicios base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071305"
---
# <a name="base-service-providers"></a>Proveedores de servicios base

Estos [*proveedores de servicios*](/windows/desktop/SecGloss/c-gly) proporcionan las funcionalidades [*básicas de tarjeta inteligente.*](/windows/desktop/SecGloss/s-gly) Se pueden usar para acceder a una única funcionalidad de tarjeta inteligente o sus interfaces COM se pueden combinar para proporcionar varias funcionalidades dentro de un único proveedor de servicios. Estos proveedores de servicios son los bloques de creación para desarrollar funcionalidad adicional para otros proveedores de servicios.

Las siguientes tareas se pueden realizar mediante las interfaces del proveedor de servicios base proporcionadas por el SDK de tarjeta inteligente.



| Tarea                                                                                                                   | Interfaces del proveedor de servicios base         | Archivo DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Conectar a una tarjeta inteligente, implemente transacciones, cierre las conexiones, y así sucesivamente.                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| Mantenga un comando APDU y [*responda a APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Consulte la base [*de datos de tarjeta inteligente*](/windows/desktop/SecGloss/s-gly). | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Busque una tarjeta inteligente o un lector.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Compile un comando ISO7816-4 APDU.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Encapsular un búfer de Istream mediante Visual Basic tipos compatibles.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

En el procedimiento siguiente se muestra un uso típico de estas interfaces de proveedor de servicios base. En este ejemplo, las interfaces [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md) se usan para realizar una transacción.

**Para realizar una transacción**

1.  Cree una instancia para todas las interfaces de proveedor de servicios base necesarias (por ejemplo, [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md)).
2.  Conectar a una tarjeta inteligente determinada mediante los métodos de la [**interfaz ISCard.**](iscard.md)
3.  Con [**ISCardISO7816**](iscardiso7816.md) y un objeto [**ISCardCmd,**](iscardcmd.md) compile un comando ISO 7816-4 llamando al **método ISCardISO7816.** El comando se encuentra en **ISCardCmd como** el comando APDU.
4.  Realice una transacción con la tarjeta llamando al método de transacción [**ISCard**](iscard.md) y pasando el objeto [**ISCardCmd**](iscardcmd.md) creado. Una vez completada la transacción, los resultados se almacenan en la APDU de respuesta de **ISCardCmd.**
5.  Interpretar la APDU de respuesta de [**ISCardCmd**](iscardcmd.md) y repetir.
6.  Liberar todas las interfaces cuando se completen las operaciones.

Para obtener información sobre el comando APDU creado dentro de los archivos DLL, vea [Building an ISO7816-4 APDU Command](building-an-iso7816-4-apdu-command.md).

 

 
