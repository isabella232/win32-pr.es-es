---
description: Consulte la base de datos de tarjetas inteligentes. Pueden proporcionar una lista de tarjetas inteligentes proporcionadas por un usuario específico, las interfaces y el proveedor de servicios principal de una tarjeta específica, los grupos de lectores definidos para el sistema y los lectores dentro de un conjunto de grupos de lectores.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funciones de consulta de base de datos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374943"
---
# <a name="smart-card-database-query-functions"></a>Funciones de consulta de base de datos de tarjeta inteligente

Las siguientes funciones consultan la base [*de datos de tarjeta inteligente*](../secgloss/s-gly.md). Pueden proporcionar una lista de tarjetas inteligentes proporcionadas por un usuario específico, [](../secgloss/r-gly.md) las interfaces y el proveedor [](../secgloss/r-gly.md) de servicios principal de una tarjeta específica, los grupos de lectores definidos para el sistema y los lectores dentro de un conjunto de grupos de lectores. [](../secgloss/p-gly.md)

Al usar estas funciones, puede consultar la base de datos completa de tarjetas inteligentes o puede restringir la búsqueda estableciendo el contexto [*de Resource Manager*](../secgloss/r-gly.md). El contexto del administrador de recursos se establece mediante una llamada a [**SCardEstablishContext antes**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) de llamar a una función de consulta.

> [!Note]  
> Sin un contexto especificado, es posible que alguna información todavía no sea accesible debido a restricciones de seguridad.

 



| Tema                                                  | Descripción                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Recupere el identificador (GUID) del [*proveedor de servicios principal*](../secgloss/p-gly.md) para la tarjeta dada. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Recuperar una lista de tarjetas introducidas previamente en el sistema por un usuario específico.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Recupere los identificadores (GUID) de las interfaces proporcionadas por una tarjeta determinada.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Recupere una lista de grupos de lectores que se han introducido previamente en el sistema.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Recupere la lista de lectores dentro de un conjunto de grupos de lectores con nombre.                                                                                                                    |



 

 

 
