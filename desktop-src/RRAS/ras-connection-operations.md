---
title: Operaciones de conexión RAS
description: Windows NT y versiones posteriores proporcionan las funciones RasPhonebookDlg y RasDialDlg que muestran la interfaz de usuario integrada para iniciar una operación de conexión RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operaciones de conexión, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e2a78d34afd5aea3670730656e97886b6a5916
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904712"
---
# <a name="ras-connection-operations"></a>Operaciones de conexión RAS

Windows NT y versiones posteriores proporcionan las funciones [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) y [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) que muestran la interfaz de usuario integrada para iniciar una operación de conexión RAS. Para la mayoría de las aplicaciones, esta es la manera preferida de iniciar una operación de conexión RAS. Windows 95 no admite actualmente estas funciones.

En el resto de esta sección se describen las funciones de bajo nivel para iniciar una conexión RAS. Estas funciones están disponibles en bothWindows NT 4,0 (y versiones posteriores) y Windows 95.

Una aplicación cliente RAS utiliza la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer una conexión a un servidor RAS. La función **rasdial** inicia la operación de conexión, que se lleva a cabo mediante el administrador de conexiones de acceso remoto.

El administrador de conexiones de acceso remoto es un servicio que controla los detalles del establecimiento de la conexión con el servidor remoto. Este servicio también proporciona al cliente información de estado durante la operación de conexión. El administrador de conexiones de acceso remoto se inicia automáticamente cuando una aplicación carga el RASAPI32.DLL.

La llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica la siguiente información cuando inicia una operación de conexión:

-   La [información de conexión](phone-book-files-and-connection-information.md) que el administrador de conexiones de acceso remoto necesita para establecer la conexión.
-   Un [controlador de notificación](notification-handlers.md) opcional que recibe notificaciones de progreso durante la operación de conexión. Si la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica un controlador de notificación, la llamada es [asincrónica](asynchronous-operations.md); de lo contrario, es [sincrónico](synchronous-operations.md).
-   Una estructura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) opcional para habilitar o deshabilitar las extensiones de la operación [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Las extensiones permiten a un cliente RAS habilitar directamente algunos valores del módem, controlar si RAS usa los prefijos y sufijos en una entrada de libreta de teléfonos, y para admitir [Estados en pausa](paused-states.md) durante la operación de conexión.

 

 