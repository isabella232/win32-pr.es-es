---
title: Establecer una conexión de acceso telefónico a Internet
description: Las siguientes funciones se usan para controlar las conexiones de módem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078234"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Establecer una conexión de acceso telefónico a Internet

Las siguientes funciones se usan para controlar las conexiones de módem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Las funciones de acceso telefónico de WinINet no admiten conexiones de doble marcado, autenticación de tarjeta inteligente ni conexiones que requieran certificación basada en el registro.

 

> [!Note]  
> A partir de Windows Vista y Windows Server 2008, las funciones de acceso telefónico de WinINet usan las [funciones RAS](/windows/desktop/RRAS/remote-access-service-functions) para establecer una conexión de acceso telefónico. WinINet admite la funcionalidad documentada en la función [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 