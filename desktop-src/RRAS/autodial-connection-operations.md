---
title: Operaciones de conexión de marcado automático
description: Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede tener acceso al host, el sistema busca la dirección en la base de datos de asignación de marcado automático.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150fa8542d1724be9d60f997db7952d6df387b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420808"
---
# <a name="autodial-connection-operations"></a>Operaciones de conexión de marcado automático

Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede tener acceso al host, el sistema busca la dirección en la base de datos de asignación de marcado automático. Si la dirección está en la base de datos, el sistema inicia una operación de marcado automático para el [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), si existe, que corresponde a la ubicación de marcado TAPI local.

La API de RAS proporciona funciones que permiten establecer y consultar parámetros de marcado automático que controlan las conexiones de marcado automático. Puede llamar a la función [**RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) para habilitar o deshabilitar la característica de marcado automático para una ubicación de marcado TAPI especificada. La función [**RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indica si la característica de marcado automático está habilitada para una ubicación de marcado TAPI especificada. Para obtener más información acerca de las ubicaciones de marcado TAPI, consulte la documentación de TAPI. Puede llamar a la función [**RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) para establecer otros parámetros de conexión de marcado automático. Por ejemplo, puede deshabilitar las conexiones de marcado automático para la sesión de inicio de sesión actual. Llame a la función [**RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) para determinar el valor actual de los parámetros de conexión de marcado automático.

El sistema proporciona una interfaz de usuario predeterminada para las operaciones de marcado automático. Sin embargo, puede crear una biblioteca de vínculos dinámicos (DLL) de marcado automático para proporcionar una interfaz de usuario personalizada para las operaciones de marcado automático que impliquen entradas de libretas de teléfonos especificadas. El archivo DLL de marcado automático debe exportar una versión ANSI y Unicode de un controlador de marcado automático [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) .

Para habilitar el controlador de marcado automático personalizado para una entrada de libreta de teléfonos, llame a la función [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer las propiedades de esa entrada. Los miembros **szAutodialDll** y **szAutodialFunc** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) que se pasan a **RasSetEntryProperties** especifican el nombre del archivo dll de marcado automático y el nombre de la función [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) , sin incluir el sufijo "A" o "W".

Cuando el sistema inicia una operación de marcado automático para una entrada de libreta de teléfonos con un controlador de marcado automático personalizado, llama a la [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)especificada. La función **RASADFunc** recibe un puntero a una estructura [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) que indica la ubicación y la ventana primaria de la ventana de la interfaz de usuario. El **RASADFunc** puede iniciar un subproceso para realizar la operación de marcado personalizada. La función **RASADFunc** devuelve **true** para indicar que se ha realizado el marcado, o bien **false** para permitir que el sistema realice el marcado. La operación de marcado personalizada debe utilizar la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para realizar el marcado real. Una vez completada la operación de marcado, la operación de marcado personalizado indica si se ha realizado correctamente o no mediante la configuración de la variable a la que señala el parámetro *lpdwRetCode* pasado a [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca).

 

 