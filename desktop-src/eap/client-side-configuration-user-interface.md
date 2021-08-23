---
title: Client-Side configuración Interfaz de usuario
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) de configuración para el protocolo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c8b067ba65312edea412ba532620e029912088e9cc61885626f8a13f5a2834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117814"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side configuración Interfaz de usuario

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) de configuración para el protocolo. La interfaz de usuario de configuración se puede implementar en el mismo archivo DLL que el protocolo de autenticación o en un archivo DLL independiente. Además, el archivo DLL que implementa la interfaz de usuario de configuración puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL para la interfaz de usuario de configuración se almacena en el valor del Registro CONFIGUI DE RAS EAP VALUENAME, en la clave \_ \_ del protocolo de \_ autenticación. Para obtener más información sobre cómo crear este valor del Registro, vea [Instalación de EAP.](eap-installation.md)

El archivo DLL de la interfaz de usuario de configuración debe exportar puntos de entrada para las siguientes funciones:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Cuando el usuario crea una entrada de configuración para una conexión determinada, ya sea para un cliente RAS o inalámbrico, el usuario puede seleccionar el protocolo de autenticación que el servicio debe usar con esa entrada. Si el protocolo de autenticación es configurable, el servicio llama a [**RasEapInvokeConfigUI para**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) invocar la interfaz de usuario de configuración. La interfaz de usuario de configuración almacena la información de configuración devuelta **por RasEapInvokeConfigUI en** la entrada de configuración.

La información de configuración debe ser genérica para todos los usuarios del equipo cliente. La información específica de un usuario o usuarios determinados no debe almacenarse en la entrada. El protocolo de autenticación debe obtener información específica del usuario mediante las funciones [de identidad o](obtaining-identity-information.md) la interfaz de usuario [interactiva](interactive-user-interface.md). El protocolo de autenticación puede almacenar esta información en el Registro si se pasa al servicio de autenticación en el *parámetro pEapOutput* [**de RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

La información de configuración tampoco debe ser específica de la máquina actual; debe ser portátil de una máquina a otra.

Cuando el servicio de autenticación llama a la [**función RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) para el protocolo de autenticación, pasa una estructura [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contiene un puntero a la información de configuración. Una vez completada la llamada a **RasEapBegin,** el servicio de autenticación llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por la información de configuración. Por lo tanto, el protocolo de autenticación debe copiar la información de configuración en un búfer de memoria privado durante la llamada a **RasEapBegin**.

El proveedor puede agregar un valor bajo la clave del Registro para el protocolo de autenticación que especifica la información de configuración predeterminada para el protocolo. El proveedor también puede agregar un valor que especifica si el usuario debe escribir información de configuración cuando crea una entrada de la libreta de teléfonos. Para obtener más información, vea [Valores del Registro del protocolo de autenticación](authentication-protocol-registry-values.md).

 

 