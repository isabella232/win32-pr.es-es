---
title: Otra información de conexión
description: Los miembros de la estructura RASDIALPARAMS también pueden especificar la siguiente información de conexión.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995362"
---
# <a name="other-connection-information"></a>Otra información de conexión

Los miembros de la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) también pueden especificar la siguiente información de conexión.

-   Un número de teléfono para invalidar el número en la entrada de la libreta de teléfonos.
-   Un número de teléfono de [devolución](callback-connections.md) de llamada al que el servidor remoto puede volver a llamar para establecer la conexión.
-   Nombre del dominio de red remoto en el que se va a producir la autenticación.

En el caso del número de devolución de llamada y el dominio, los miembros de [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) pueden indicar que ras debe usar la información de la entrada de la libreta de teléfonos, o bien puede proporcionar información que invalide los datos del libro de teléfono.

Un cliente RAS puede usar el parámetro *lpRasDialExtensions* de la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para controlar si ras usa un prefijo o sufijo de número de teléfono especificado en una entrada de libreta de teléfonos.

 

 