---
title: Obtener información de identidad
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de función que obtenga información de identificación inicial para el usuario que solicita la autenticación.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605825"
---
# <a name="obtaining-identity-information"></a>Obtener información de identidad

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de función que obtenga información de identificación inicial para el usuario que solicita la autenticación.

El proveedor debe implementar las siguientes funciones.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Estas funciones se pueden implementar en el mismo archivo DLL que el protocolo de autenticación o en un archivo DLL independiente. Además, el archivo DLL que implementa las funciones de identidad puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL para estas funciones se almacena en el valor del Registro [ \_ RAS EAP \_ VALUENAME \_ IDENTITY,](authentication-protocol-registry-values.md) en la clave del protocolo de autenticación. Para obtener más información sobre cómo crear este valor del Registro, vea [Instalación de EAP.](eap-installation.md)

La [**función RasEapGetIdentity normalmente**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) muestra una interfaz de usuario (UI) para obtener información de identidad del usuario. Sin embargo, si el *parámetro dwFlags* contiene la marca NO INTERACTIVA \_ RAS EAP \_ \_ \_ FLAG, **RasEapGetIdentity** no debería mostrar una interfaz de usuario.

Si [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) muestra una interfaz de usuario, la interfaz de usuario debe admitir mensajes [**WM \_ COMMAND**](../menurc/wm-command.md) donde el valor de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) es igual a IDCANCEL.

El servicio de autenticación llama a [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) si el valor DE [ \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG](authentication-protocol-registry-values.md) de RAS que se encuentra en el Registro para este EAP está establecido en cero. Si RAS \_ EAP VALUENAME INVOKE NAMEDLG no está presente o está presente y está establecido en uno, el servicio de autenticación muestra el cuadro de diálogo nombre de usuario del sistema \_ \_ \_ estándar.

Además de RAS EAP VALUENAME INVOKE NAMEDLG, el proveedor de EAP puede crear un valor \_ \_ \_ \_ relacionado, [RAS EAP \_ \_ VALUENAME INVOKE \_ \_ PWDDLG](authentication-protocol-registry-values.md), en el Registro. Si este valor está presente y se establece en cero, el servicio no mostrará el cuadro de diálogo de contraseña del sistema estándar. Este valor es útil al implementar un método biométrico, como un examen de huella digital, para autenticar al usuario. Si los valores INVOKE NAMEDLG y RAS \_ \_ EAP \_ \_ \_ \_ VALUENAME INVOKE \_ \_ PWDDLG son cero, se podría usar una interfaz de usuario de identidad para obtener la información biométrica y de identidad. Sin embargo, si solo EL VALOR DE EAP DE RASNAME INVOKE PWDDLG es cero, el servicio de autenticación no llamará \_ \_ a \_ \_ [**RasEapGetIdentity.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) En este caso, podría usar la [interfaz de usuario interactiva para](interactive-user-interface.md) obtener la información biométrica.

Para obtener más información sobre estos valores del Registro, vea [Valores del Registro del protocolo de autenticación](authentication-protocol-registry-values.md).

La información obtenida por [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se pasa al protocolo de autenticación durante la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Los miembros **pszIdentity** y **pUserData** de la estructura PPP EAP INPUT apuntan a [**\_ \_ la**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) información. Para guardar esta información en el Registro en el equipo cliente, el protocolo de autenticación debe devolver la información del parámetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Después de llamar a [**RasEapBegin,**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))el servicio de autenticación llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por estos datos. Por lo tanto, el protocolo de autenticación debe copiar la información en un búfer de memoria privado durante la llamada a **RasEapBegin**.

 

 