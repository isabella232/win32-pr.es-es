---
title: Operaciones de conexión autodial
description: Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede acceder al host, el sistema busca la dirección en la base de datos de asignación AutoDial.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f65f62121d631dcf035e641c9d0d4d89850d7673e1c47b82ff4a4889dff49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030505"
---
# <a name="autodial-connection-operations"></a>Operaciones de conexión autodial

Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede acceder al host, el sistema busca la dirección en la base de datos de asignación AutoDial. Si la dirección está en la base de datos, el sistema inicia una operación AutoDial para [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), si existe, que corresponde a la ubicación de marcado tapI local.

La API ras proporciona funciones que permiten establecer y consultar parámetros AutoDial que controlan las conexiones AutoDial. Puede llamar a la [**función RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) para habilitar o deshabilitar la característica AutoDial para una ubicación de marcado TAPI especificada. La [**función RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indica si la característica AutoDial está habilitada para una ubicación de marcado TAPI especificada. Para más información sobre las ubicaciones de marcado de TAPI, consulte la documentación de TAPI. Puede llamar a la [**función RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) para establecer otros parámetros de conexión AutoDial. Por ejemplo, puede deshabilitar las conexiones AutoDial para la sesión de inicio de sesión actual. Llame a [**la función RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) para determinar el valor actual de los parámetros de conexión AutoDial.

El sistema proporciona una interfaz de usuario predeterminada para las operaciones de marcado automático. Sin embargo, puede crear una biblioteca de vínculos dinámicos (DLL) de AutoDial para proporcionar una interfaz de usuario personalizada para las operaciones de marcado automático que implican entradas especificadas de la libreta de teléfonos. El archivo DLL de AutoDial debe exportar una versión ANSI y una versión Unicode de un controlador [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) AutoDial.

Para habilitar el controlador de AutoDial personalizado para una entrada de libreta de teléfonos, llame a la [**función RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer las propiedades de esa entrada. Los **miembros szAutodialDll** y **szAutodialFunc** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) pasados a **RasSetEntryProperties** especifican el nombre de la DLL autodial y el nombre de la función [**RASADFunc,**](/windows/desktop/api/Ras/nc-ras-rasadfunca) excepto el sufijo "A" o "W".

Cuando el sistema inicia una operación AutoDial para una entrada de la libreta de teléfonos con un controlador AutoDial personalizado, llama al [**objeto RASADFunc especificado.**](/windows/desktop/api/Ras/nc-ras-rasadfunca) La **función RASADFunc** recibe un puntero a una estructura [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) que indica la ubicación y la ventana primaria de la ventana de la interfaz de usuario. **RasADFunc** puede iniciar un subproceso para realizar la operación de marcado personalizada. La **función RASADFunc** devuelve **TRUE** para indicar que se ha hecho cargo de la marcación, o **FALSE** para permitir que el sistema realice la marcación. La operación de marcado personalizada debe usar la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para realizar la marcación real. Una vez completada la operación de marcado, la operación de marcado personalizada indica que se ha realizado correctamente o no estableciendo la variable a la que apunta el parámetro *lpdwRetCode* pasado a [**RASADFunc.**](/windows/desktop/api/Ras/nc-ras-rasadfunca)

 

 