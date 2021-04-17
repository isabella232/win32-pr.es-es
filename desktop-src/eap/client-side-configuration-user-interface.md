---
title: Interfaz de usuario de configuración de Client-Side
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) de configuración para el protocolo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7296f6afd8fd84f287b6c2c7085e5ed92685f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358891"
---
# <a name="client-side-configuration-user-interface"></a>Interfaz de usuario de configuración de Client-Side

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) de configuración para el protocolo. La interfaz de usuario de configuración se puede implementar en el mismo archivo DLL que el protocolo de autenticación, o en un archivo DLL independiente. Además, el archivo DLL que implementa la interfaz de usuario de configuración puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL de la interfaz de usuario de configuración se almacena en el \_ \_ \_ valor del registro ras EAP ValueName CONFIGUI, en la clave del Protocolo de autenticación. Para obtener más información acerca de cómo crear este valor del registro, vea [instalación de EAP](eap-installation.md).

El archivo DLL de la interfaz de usuario de configuración debe exportar puntos de entrada para las siguientes funciones:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Cuando el usuario crea una entrada de configuración para una conexión determinada, ya sea para un cliente RAS o inalámbrico, el usuario puede seleccionar el protocolo de autenticación que el servicio debe usar con esa entrada. Si el protocolo de autenticación es configurable, el servicio llama a [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) para invocar la interfaz de usuario de configuración. La interfaz de usuario de configuración almacena la información de configuración devuelta por **RasEapInvokeConfigUI** en la entrada de configuración.

La información de configuración debe ser genérica para todos los usuarios del equipo cliente. La información específica de un usuario o usuarios concretos no debe almacenarse en la entrada. El protocolo de autenticación debe obtener información específica del usuario mediante las [funciones de identidad](obtaining-identity-information.md) o la [interfaz de usuario interactiva](interactive-user-interface.md). El protocolo de autenticación puede almacenar esta información en el registro pasándola al servicio de autenticación en el parámetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

La información de configuración tampoco debe ser específica del equipo actual; debe ser portátil de un equipo a un equipo.

Cuando el servicio de autenticación llama a la función [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) para el protocolo de autenticación, pasa una estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contiene un puntero a la información de configuración. Una vez finalizada la llamada a **RasEapBegin** , el servicio de autenticación llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por la información de configuración. Por lo tanto, el protocolo de autenticación debe copiar la información de configuración en un búfer de memoria privado durante la llamada a **RasEapBegin**.

El proveedor puede Agregar un valor en la clave del registro para el protocolo de autenticación que especifica la información de configuración predeterminada para el protocolo. El proveedor también puede Agregar un valor que especifica si el usuario debe escribir información de configuración al crear una entrada de libreta de teléfonos. Para obtener más información, vea [valores del registro del Protocolo de autenticación](authentication-protocol-registry-values.md).

 

 