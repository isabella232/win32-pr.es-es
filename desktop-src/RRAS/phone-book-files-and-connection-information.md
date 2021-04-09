---
title: Phone-Book de archivos e información de conexión
description: Una llamada RasDial debe especificar la información que el administrador de conexiones de acceso remoto necesita para establecer la conexión.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149521"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book de archivos e información de conexión

Una llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) debe especificar la información que el administrador de conexiones de acceso remoto necesita para establecer la conexión. Normalmente, la llamada **rasdial** proporciona la información de conexión mediante la especificación de una entrada de la libreta de teléfonos. La información de conexión de una entrada de libreta de teléfonos incluye números de teléfono, velocidades de BPS, [información de autenticación de usuario](user-authentication-information.md)y [otra información de conexión](other-connection-information.md).

Un cliente RAS usa los parámetros de la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar un archivo de libreta de teléfonos y una entrada en ese archivo. El parámetro *lpszPhonebookPath* puede especificar el nombre de un archivo de libreta de teléfonos o puede ser **null** para indicar que se debe usar el archivo de libreta de teléfonos predeterminado. El parámetro *lpRasDialParams* apunta a una estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) que especifica el nombre de la entrada de la libreta de teléfonos que se va a usar.

Para mostrar una lista de entradas de libreta de teléfonos desde las que el usuario puede seleccionar una conexión, un cliente RAS puede llamar a la función [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) para enumerar las entradas de un archivo de libreta de teléfonos.

Para establecer una conexión sin usar una entrada de libreta de teléfonos, la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) puede especificar una cadena vacía para el miembro **szEntryName** de la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . El miembro **RASDIALPARAMS. szPhoneNumber** debe contener el número al que llamar. En este caso, el administrador de conexiones de acceso remoto utiliza el primer puerto de módem disponible y los valores predeterminados para el resto de configuraciones.

 

 