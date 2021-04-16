---
title: Interfaz de usuario interactiva
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) interactiva para el protocolo.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761799969f4e439a65534ab551f09b3788e95ba7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714357"
---
# <a name="interactive-user-interface"></a>Interfaz de usuario interactiva

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario (UI) interactiva para el protocolo. La interfaz de usuario interactiva permite que el protocolo de autenticación obtenga información adicional del usuario según sea necesario durante el transcurso de la sesión de autenticación.

La interfaz de usuario interactiva se puede implementar en el mismo archivo DLL que el protocolo de autenticación o en un archivo DLL independiente. Además, el archivo DLL que implementa la interfaz de usuario interactiva puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL para la interfaz de usuario interactiva se almacena en el valor del registro [ras \_ EAP \_ ValueName \_ INTERACTIVEUI](authentication-protocol-registry-values.md) , en la clave del Protocolo de autenticación. Para obtener más información acerca de cómo crear este valor del registro, vea [instalación de EAP](eap-installation.md).

El archivo DLL de la interfaz de usuario interactiva debe exportar puntos de entrada para las siguientes funciones:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

La interfaz de usuario interactiva debe admitir mensajes de [**\_ comandos de WM**](../menurc/wm-command.md) en los que [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) es igual a IDCANCEL.

Para mostrar la interfaz de usuario interactiva, el protocolo de autenticación debe establecer el miembro **fInvokeInteractiveUI** de la estructura de [**\_ \_ salida EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en **true**. Opcionalmente, el protocolo de autenticación también puede establecer los miembros **pUIContextData** y **dwSizeOfUIContextData** en **true** . El servicio de autenticación usa los valores de estos miembros para pasar datos de contexto a la interfaz de usuario interactiva. El protocolo de autenticación devuelve la estructura de **\_ \_ salida EAP de PPP** como parámetro en la función [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) .

El servicio de autenticación invoca la interfaz de usuario interactiva mediante una llamada a [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). A continuación, el servicio pasa el protocolo de autenticación un puntero a los datos devueltos por la interfaz de usuario interactiva en la siguiente llamada a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). El puntero se pasa como un miembro de una estructura de [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Una vez que **RasEapMakeMessage** devuelve, el servicio llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por la información. Por lo tanto, el protocolo de autenticación debe copiar la información en un búfer de memoria privado durante la llamada a **RasEapMakeMessage**.

 

 