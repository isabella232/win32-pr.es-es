---
title: Phone-Book archivos y la información de conexión
description: Una llamada RasDial debe especificar la información que el Connection Manager remoto necesita para establecer la conexión.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265572"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book archivos y la información de conexión

Una [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) debe especificar la información que el Connection Manager remoto necesita para establecer la conexión. Normalmente, la **llamada RasDial** proporciona la información de conexión especificando una entrada de la libreta de teléfonos. La información de conexión de una entrada de la [](user-authentication-information.md)libreta de teléfonos incluye números de teléfono, tasas de bps, información de autenticación de usuario y [otra información de conexión](other-connection-information.md).

Un cliente RAS usa los parámetros de la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar un archivo de libreta de teléfonos y una entrada en ese archivo. El *parámetro lpszPhonebookPath* puede especificar el nombre de un archivo de libreta de teléfonos o puede ser **NULL** para indicar que se debe usar el archivo de libreta de teléfonos predeterminado. El *parámetro lpRasDialParams* apunta a una estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) que especifica el nombre de la entrada de la libreta telefónica que se usará.

Para mostrar una lista de entradas de la libreta de teléfonos desde las que el usuario puede seleccionar una conexión, un cliente RAS puede llamar a la función [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) para enumerar las entradas en un archivo de libreta de teléfonos.

Para realizar una conexión sin usar una entrada de la libreta de teléfonos, la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) puede especificar una cadena vacía para el **miembro szEntryName** de la estructura [**RASDIALPARAMS.**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) El **miembro RASDIALPARAMS.szPhoneNumber** debe contener el número al que se debe llamar. En este caso, el acceso remoto Connection Manager el primer puerto de módem disponible y los valores predeterminados para todas las demás configuraciones.

 

 