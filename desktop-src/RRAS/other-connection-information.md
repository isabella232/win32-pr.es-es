---
title: Otra información de conexión
description: Los miembros de la estructura RASDIALPARAMS también pueden especificar la siguiente información de conexión.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253694"
---
# <a name="other-connection-information"></a>Otra información de conexión

Los miembros de la [**estructura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) también pueden especificar la siguiente información de conexión.

-   Número de teléfono para invalidar el número de la entrada de la libreta de teléfonos.
-   Número [de teléfono de devolución](callback-connections.md) de llamada al que el servidor remoto puede llamar para establecer la conexión.
-   Nombre del dominio de red remoto en el que se va a producir la autenticación.

Para el número de devolución de llamada y el dominio, los miembros [**de RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) pueden indicar que RAS debe usar la información de la entrada de la libreta de teléfonos o puede proporcionar información que invalide los datos de la libreta de teléfonos.

Un cliente RAS puede usar el parámetro *lpRasDialExtensions* de la función [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para controlar si RAS usa un prefijo o sufijo de número de teléfono especificado en una entrada de la libreta de teléfono.

 

 