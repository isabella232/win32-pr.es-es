---
description: Consultar la base de datos de tarjeta inteligente. Pueden proporcionar una lista de tarjetas inteligentes suministradas por un usuario específico, las interfaces y el proveedor de servicios principal de una tarjeta específica, los grupos de lectores definidos para el sistema y los lectores dentro de un conjunto de grupos de lectores.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funciones de consulta de bases de datos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278264"
---
# <a name="smart-card-database-query-functions"></a>Funciones de consulta de bases de datos de tarjeta inteligente

Las siguientes funciones consultan la [*base de datos de tarjeta inteligente*](../secgloss/s-gly.md). Pueden proporcionar una lista de tarjetas inteligentes suministradas por un usuario específico, las interfaces y el [*proveedor de servicios principal*](../secgloss/p-gly.md) de una tarjeta específica, los [*grupos de lectores*](../secgloss/r-gly.md) definidos para el sistema y los [*lectores*](../secgloss/r-gly.md) dentro de un conjunto de grupos de lectores.

Cuando se usan estas funciones, se puede consultar la base de datos completa de la tarjeta inteligente, o bien se puede restringir la búsqueda estableciendo el [*contexto del administrador de recursos*](../secgloss/r-gly.md). El contexto del administrador de recursos se establece mediante una llamada a [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) antes de llamar a una función de consulta.

> [!Note]  
> Sin un contexto especificado, es posible que no se pueda tener acceso a cierta información debido a restricciones de seguridad.

 



| Tema                                                  | Descripción                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Recupera el identificador (GUID) del proveedor de [*servicios principal*](../secgloss/p-gly.md) de la tarjeta especificada. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Recupera una lista de tarjetas introducidas previamente en el sistema por un usuario específico.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Recupera los identificadores (GUID) de las interfaces proporcionadas por una tarjeta determinada.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Recupera una lista de grupos de lector que se han introducido previamente en el sistema.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Recupera la lista de lectores dentro de un conjunto de grupos de lectores con nombre.                                                                                                                    |



 

 

 
