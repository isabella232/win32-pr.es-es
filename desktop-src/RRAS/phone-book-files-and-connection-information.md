---
title: Phone-Book e información de conexión
description: Una llamada RasDial debe especificar la información que el Connection Manager remoto necesita para establecer la conexión.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a4bc7831673fb51a4c48177692674d6d2560ccec327dd3260dacb49e8ecfa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029125"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book e información de conexión

Una [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) debe especificar la información que el Connection Manager remoto necesita para establecer la conexión. Normalmente, la **llamada RasDial** proporciona la información de conexión especificando una entrada de la libreta de teléfonos. La información de conexión de una entrada de la [](user-authentication-information.md)libreta de teléfonos incluye números de teléfono, tasas de bps, información de autenticación de usuario y [otra información de conexión](other-connection-information.md).

Un cliente RAS usa los parámetros de la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar un archivo de libreta de teléfono y una entrada en ese archivo. El *parámetro lpszPhonebookPath* puede especificar el nombre de un archivo de libreta de teléfonos o puede ser **NULL** para indicar que se debe usar el archivo de libreta de teléfono predeterminado. El *parámetro lpRasDialParams* apunta a una estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) que especifica el nombre de la entrada de la libreta de teléfonos que se usará.

Para mostrar una lista de entradas de la libreta de teléfonos desde las que el usuario puede seleccionar una conexión, un cliente RAS puede llamar a la función [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) para enumerar las entradas de un archivo de libreta de teléfonos.

Para realizar una conexión sin usar una entrada de libreta de teléfonos, la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) puede especificar una cadena vacía para el **miembro szEntryName** de la estructura [**RASDIALPARAMS.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) El **miembro RASDIALPARAMS.szPhoneNumber** debe contener el número al que se debe llamar. En este caso, el acceso remoto Connection Manager el primer puerto de módem disponible y los valores predeterminados para todas las demás configuraciones.

 

 