---
title: Subentradas y conexiones multivínculo
description: Windows NT Server 4,0 proporciona compatibilidad con las subentradas de libreta de teléfonos, que habilitan las conexiones multivínculo. Una conexión multivínculo combina el ancho de banda de varias conexiones para proporcionar una sola conexión con un ancho de banda mayor.
ms.assetid: 19cf6e1a-cdba-47e4-8d8f-d6030ed6f9e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1970e2e2ad668b376b1097aa20cd18986fb605a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359288"
---
# <a name="subentries-and-multilink-connections"></a>Subentradas y conexiones multivínculo

Windows NT Server 4,0 proporciona compatibilidad con las subentradas de libreta de teléfonos, que habilitan las conexiones multivínculo. Una conexión multivínculo combina el ancho de banda de varias conexiones para proporcionar una sola conexión con un ancho de banda mayor.

Una entrada de libreta de teléfonos RAS puede tener cero o más subentradas. La función [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) recupera una estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) que incluye información sobre las subentradas de una entrada de libreta de teléfonos. El miembro **dwSubEntries** de la estructura **RASENTRY** indica el número de subentradas. Inicialmente, las entradas de la libreta de teléfonos no tienen subentradas. Para agregar subentradas a una entrada de la libreta de teléfonos, utilice la función [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) .

Las propiedades de cada subentrada incluyen un número de teléfono y el nombre y tipo del dispositivo TAPI que se va a utilizar al marcar la subentrada. Además, una subentrada puede incluir una lista de números de teléfono alternativos para marcar si RAS no puede establecer una conexión con el número principal. Las funciones [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) y [**RasGetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa) usan la estructura [**RASSUBENTRY**](/previous-versions/windows/desktop/legacy/aa377839(v=vs.85)) para establecer y recuperar las propiedades de una entrada de libreta de teléfonos especificada. Las subentradas se identifican mediante un índice basado en uno.

Puede llamar a la función [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para configurar una entrada ras Multilink para que conecte todas las subentradas cuando se marque por primera vez. Como alternativa, puede configurar una entrada para proporcionar ancho de banda variable. En este caso, RAS conecta una única subentrada inicialmente y, a continuación, conecta o desconecta las subentradas adicionales según sea necesario. En el caso de una conexión Multilink de ancho de banda variable, puede usar la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para especificar la subentrada inicial que se va a conectar cuando llame a la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Al usar la función [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para conectar una entrada de hipervínculo, puede usar la estructura [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar la subentrada inicial que se va a conectar.

En el caso de una conexión Multilink de ancho de banda variable, use la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) con la función [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para especificar los parámetros de conexión y desconexión de las subentradas individuales. RAS conecta una subentrada adicional cuando el ancho de banda utilizado supera un porcentaje especificado del ancho de banda disponible para un intervalo especificado.

Si llama a la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer una conexión de vínculos múltiples, puede especificar una función de devolución de llamada [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) para recibir notificaciones sobre la conexión. **RasDialFunc2** es similar a la función de devolución de llamada [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) , salvo que proporciona información adicional para una conexión de vínculos múltiples, como el índice de la subentrada que causó la notificación. RAS llama a la función **RasDialFunc2** cuando conecta o desconecta una subentrada.

Puede usar un identificador de conexión de **HRASCONN** para colgar o recuperar información sobre una conexión de vínculos múltiples. Puede obtener un identificador de conexión para cada una de las conexiones de subentrada que componen el multivínculo, así como para la conexión combinada de hipervínculos. Cuando se llama a la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer una conexión de multivínculo, **rasdial** devuelve un identificador a la conexión combinada de hipervínculos. Del mismo modo, [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) devuelve el identificador de multivínculo combinado al enumerar las conexiones. Para obtener un identificador de una de las conexiones de subentrada en una conexión de multivínculo, llame a la función [**RasGetSubEntryHandle**](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea) .

Puede usar el identificador de conexión Multilink combinado y los identificadores de conexión de subentrada en las funciones [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa), [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)y [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) . La llamada a **RasHangUp** con un identificador de multivínculo combinado finaliza toda la conexión; Si se llama con un identificador de subentrada, solo se cuelga esa conexión de subentrada. Del mismo modo, **RasGetConnectStatus** devuelve información de la conexión individual o combinada, dependiendo del identificador especificado. La información de proyección devuelta por **RasGetProjectionInfo** para una entrada de hipervínculo es la misma para cada uno de los identificadores de conexión de subentrada que para el identificador de conexión principal.

 

 