---
title: Operaciones de conexión RAS
description: Windows NT y versiones posteriores proporcionan las funciones RasPhonebookDlg y RasDialDlg que muestran la interfaz de usuario integrada para iniciar una operación de conexión RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operaciones de conexión, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868465"
---
# <a name="ras-connection-operations"></a>Operaciones de conexión RAS

Windows NT y versiones posteriores proporcionan las funciones [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) y [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) que muestran la interfaz de usuario integrada para iniciar una operación de conexión RAS. Para la mayoría de las aplicaciones, esta es la manera preferida de iniciar una operación de conexión RAS. Windows 95 no admite actualmente estas funciones.

En el resto de esta sección se describen las funciones de bajo nivel para iniciar una conexión RAS. Estas funciones están disponibles en Windows NT 4.0 (y versiones posteriores) y Windows 95.

Una aplicación cliente RAS usa la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer una conexión con un servidor RAS. La **función RasDial** inicia la operación de conexión, que luego lleva a cabo el administrador de acceso Connection Manager.

El servicio Connection Manager remoto es un servicio que controla los detalles del establecimiento de la conexión con el servidor remoto. Este servicio también proporciona al cliente información de estado durante la operación de conexión. El acceso remoto Connection Manager se inicia automáticamente cuando una aplicación carga el RASAPI32.DLL.

La [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica la siguiente información cuando inicia una operación de conexión:

-   La [información de conexión](phone-book-files-and-connection-information.md) que el acceso Connection Manager necesita para establecer la conexión.
-   Un controlador [de notificaciones opcional](notification-handlers.md) que recibe notificaciones de progreso durante la operación de conexión. Si la [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica un controlador de notificaciones, la llamada es [asincrónica](asynchronous-operations.md); de lo contrario, es [sincrónico.](synchronous-operations.md)
-   Estructura [**OPCIONAL RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) para habilitar o deshabilitar las extensiones de la [**operación RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Las extensiones permiten a un cliente RAS habilitar directamente algunas configuraciones de módem, controlar si RAS usa [](paused-states.md) los prefijos y sufijos en una entrada de la libreta de teléfonos y admitir estados en pausa durante la operación de conexión.

 

 