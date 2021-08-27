---
description: Administre la base de datos de tarjeta inteligente, actualizando la base de datos mediante un contexto de Resource Manager especificado.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funciones de administración de bases de datos de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b107663df8b80b5883c9ce9b3f045e8d7913ac92b5acb23d9ae758dafa2ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917811"
---
# <a name="smart-card-database-management-functions"></a>Funciones de administración de bases de datos de tarjetas inteligentes

Las siguientes funciones administran la base [*de datos de tarjeta inteligente*](../secgloss/s-gly.md), actualizando la base de datos mediante un contexto de Resource Manager [*especificado.*](../secgloss/r-gly.md)

> [!Note]  
> La seguridad de la base de datos se mantiene mediante la colocación de restricciones de acceso en la base de datos, en lugar de agregar mecanismos de seguridad al [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md).

 



| Tema                                                            | Descripción                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | Agregue un [*lector*](../secgloss/r-gly.md) a un [*grupo de lectores*](../secgloss/r-gly.md). |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | Quite una tarjeta inteligente del sistema.                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | Quite un lector del sistema.                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | Quite un grupo de lectores del sistema.                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | Introduzca una nueva tarjeta en el sistema.                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | Introduzca un nuevo lector en el sistema.                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | Introduzca un nuevo grupo de lectores en el sistema.                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | Quitar un lector de un grupo de lectores.                                                                                                                                    |



 

 

 
