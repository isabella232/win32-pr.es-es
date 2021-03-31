---
description: Los certificados se conceden según las directivas que definen los criterios que los solicitantes deben cumplir para recibir un certificado.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Independencia de la Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360906"
---
# <a name="policy-independence"></a>Independencia de la Directiva

Los certificados se conceden según las directivas que definen los criterios que los solicitantes deben cumplir para recibir un certificado. Por ejemplo, una Directiva puede ser conceder certificados comerciales solo si los solicitantes presentan su identificación en persona. Otra directiva puede conceder [*credenciales*](../secgloss/c-gly.md) basadas en solicitudes de correo electrónico. Una agencia que emite tarjetas de crédito puede optar por consultar una base de datos y realizar consultas telefónicas antes de emitir una tarjeta.

Las directivas se implementan en módulos de directivas escritos en C++, C o Visual Basic. Las funciones de servicios de Certificate Server están aisladas de los cambios de la Directiva que puede implementar una agencia. Los cambios en la Directiva se pueden implementar completamente en el código del módulo de directivas del servidor. Una [*entidad de certificación*](../secgloss/c-gly.md) (CA) empresarial solo debe usar el módulo de directivas empresariales proporcionado por Microsoft.

 

 
