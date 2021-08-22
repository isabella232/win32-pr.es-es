---
title: Interactivo Interfaz de usuario
description: El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario interactiva para el protocolo.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f35ac3492e45e80721f800925a003edbb8116ac8c199a1b633e08a28de675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117785"
---
# <a name="interactive-user-interface"></a>Interactivo Interfaz de usuario

El proveedor que implementa el protocolo de autenticación también puede proporcionar una interfaz de usuario interactiva para el protocolo. La interfaz de usuario interactiva permite que el protocolo de autenticación obtenga información adicional del usuario según sea necesario durante el transcurso de la sesión de autenticación.

La interfaz de usuario interactiva se puede implementar en el mismo archivo DLL que el protocolo de autenticación o en un archivo DLL independiente. Además, el archivo DLL que implementa la interfaz de usuario interactiva puede admitir más de un protocolo de autenticación. La ruta de acceso al archivo DLL para la interfaz de usuario interactiva se almacena en el valor del Registro [INTERACTIVEUI DE RAS \_ EAP \_ VALUENAME, \_ ](authentication-protocol-registry-values.md) en la clave del protocolo de autenticación. Para obtener más información sobre cómo crear este valor del Registro, vea [Instalación de EAP.](eap-installation.md)

El archivo DLL de la interfaz de usuario interactiva debe exportar puntos de entrada para las siguientes funciones:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

La interfaz de usuario interactiva debe admitir [**mensajes WM \_ COMMAND**](../menurc/wm-command.md) donde [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) es igual a IDCANCEL.

Para mostrar la interfaz de usuario interactiva, el protocolo de autenticación debe establecer el miembro **fInvokeInteractiveUI** de la estructura [**PPP EAP \_ \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) en **TRUE.** El protocolo de autenticación también puede establecer los miembros **pUIContextData** y **dwSizeOfUIContextData** en **TRUE.** El servicio de autenticación usa los valores de estos miembros para pasar datos de contexto a la interfaz de usuario interactiva. El protocolo de autenticación devuelve la **estructura \_ PPP EAP \_ OUTPUT** como parámetro en la [**función RasEapMakeMessage.**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))

El servicio de autenticación invoca la interfaz de usuario interactiva mediante una [**llamada a RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). A continuación, el servicio pasa al protocolo de autenticación un puntero a los datos devueltos por la interfaz de usuario interactiva en la llamada subsiguiente a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). El puntero se pasa como miembro de una estructura [**\_ PPP EAP \_ INPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Después **de que rasEapMakeMessage** vuelva, el servicio llama a [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) para liberar la memoria ocupada por la información. Por lo tanto, el protocolo de autenticación debe copiar la información en un búfer de memoria privada durante la llamada a **RasEapMakeMessage**.

 

 