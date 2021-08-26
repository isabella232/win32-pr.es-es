---
title: Establecimiento de una conexión de acceso telefónico a Internet
description: Las siguientes funciones se usan para controlar las conexiones de módem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955595"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Establecimiento de una conexión de acceso telefónico a Internet

Las siguientes funciones se usan para controlar las conexiones de módem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Las funciones de acceso telefónico de WinINet no admiten conexiones de doble marcado, autenticación de Tarjeta inteligente ni conexiones que requieran certificación basada en el registro.

 

> [!Note]  
> A partir de Windows Vista y Windows Server 2008, las funciones de acceso telefónico de WinINet usan las funciones [RAS](/windows/desktop/RRAS/remote-access-service-functions) para establecer una conexión de acceso telefónico. WinINet admite la funcionalidad documentada en la [**función RasDialDlg.**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga)

 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 