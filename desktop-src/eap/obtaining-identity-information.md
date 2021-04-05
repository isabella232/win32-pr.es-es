---
title: Obtención de información de identidad
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de función que obtiene la información de identificación inicial para el usuario que solicita la autenticación.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9519da9d66937fd25245fe78f12ef34c3c0ad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077593"
---
# <a name="obtaining-identity-information"></a>Obtención de información de identidad

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de función que obtiene la información de identificación inicial para el usuario que solicita la autenticación.

El proveedor debe implementar las siguientes funciones.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Estas funciones se pueden implementar en el mismo archivo DLL que el protocolo de autenticación o en un archivo DLL independiente. Además, el archivo DLL que implementa las funciones de identidad puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL de estas funciones se almacena en el valor del registro de [ \_ \_ \_ identidad de EAP de Ras](authentication-protocol-registry-values.md) , en la clave del Protocolo de autenticación. Para obtener más información acerca de cómo crear este valor del registro, vea [instalación de EAP](eap-installation.md).

La función [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) normalmente muestra una interfaz de usuario (UI) para obtener información de identidad para el usuario. Sin embargo, si el parámetro *dwFlags* contiene la \_ marca \_ no interactiva de marcador EAP ras \_ \_ , **RasEapGetIdentity** no debe mostrar una interfaz de usuario.

Si [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) muestra una interfaz de usuario, la interfaz de usuario debe admitir mensajes de [**\_ comandos de WM**](../menurc/wm-command.md) en los que el valor de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) sea igual a IDCANCEL.

El servicio de autenticación llama a [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) si el valor [ \_ \_ \_ \_ NAMEDLG del ValueName EAP de Ras](authentication-protocol-registry-values.md) que se encuentra en el registro para este EAP está establecido en cero. Si \_ la invocación de NAMEDLG de EAP de Ras \_ \_ \_ no está presente o está presente y está establecida en uno, el servicio de autenticación muestra el cuadro de diálogo nombre de usuario estándar del sistema.

Además de \_ \_ la invocación de un ValueName EAP de Ras \_ \_ NAMEDLG, el proveedor de EAP puede crear un valor relacionado, la [ \_ \_ \_ invocación de ValueName \_ EAP de Ras PWDDLG](authentication-protocol-registry-values.md), en el registro. Si este valor está presente y se establece en cero, el servicio no mostrará el cuadro de diálogo contraseña del sistema estándar. Este valor es útil cuando se implementa un método biométrico, como un examen de huellas digitales para autenticar al usuario. Si los valores de la invocación de NAMEDLG y el valor de PWDDLG de EAP de ras de RAS \_ \_ \_ \_ \_ \_ \_ \_ son cero, se podría usar una interfaz de usuario de identidad para obtener la información de identidades y biométricas. Sin embargo, si solo \_ la invocación de PWDDLG de EAP de Ras \_ \_ \_ es cero, el servicio de autenticación no llamará a [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). En este caso, puede usar la [interfaz de usuario interactiva](interactive-user-interface.md) para obtener la información biométrica.

Para obtener más información sobre estos valores del registro, consulte [valores del registro del Protocolo de autenticación](authentication-protocol-registry-values.md).

La información obtenida por [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se pasa al Protocolo de autenticación durante la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Los miembros **pszIdentity** y **pUserData** de la estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) apuntan a la información. Para guardar esta información en el registro del equipo cliente, el protocolo de autenticación debe devolver la información en el parámetro *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Después de la llamada a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), el servicio de autenticación llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por estos datos. Por lo tanto, el protocolo de autenticación debe copiar la información en un búfer de memoria privado durante la llamada a **RasEapBegin**.

 

 