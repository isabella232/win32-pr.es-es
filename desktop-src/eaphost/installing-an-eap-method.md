---
title: Instalación de un método EAP
description: Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecuta EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790864"
---
# <a name="installing-an-eap-method"></a>Instalación de un método EAP

Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecuta EAPHost.

-   Implemente [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para el archivo DLL del método EAP. Estas funciones agregan y quitan las claves del registro adecuadas para el método EAP durante el proceso de instalación y (desinstalación).

    Para obtener información sobre las claves del registro específicas asociadas a la instalación de un método EAP, consulte el tema [configuración del registro para métodos EAP](registry-keys-for-eap-methods.md) .

-   Instale el archivo DLL que contiene la implementación del método EAP con el siguiente comando de la consola.

     *&lt; Nombre &gt;* deregsvr32.exedll

    Para desinstalar el archivo DLL, use el siguiente comando de la consola:

    **regsvr32.exe** **/u** *&lt; nombre &gt; del archivo dll*

-   Reinicie el servicio EAPHost.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> </dl>

 

 