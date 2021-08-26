---
title: Instalación de un método EAP
description: Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecute EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021585"
---
# <a name="installing-an-eap-method"></a>Instalación de un método EAP

Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecute EAPHost.

-   Implemente [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer para**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) el archivo DLL del método EAP. Estas funciones agregan y quitan las claves del Registro adecuadas para el método EAP durante el proceso de instalación y (desinstalación).

    Para obtener información sobre las claves del Registro específicas asociadas a la instalación de un método EAP, vea el tema Configuración del Registro [para métodos EAP.](registry-keys-for-eap-methods.md)

-   Instale el archivo DLL que contiene la implementación del método EAP con el siguiente comando de consola.

    **regsvr32.exe** *&lt; dll &gt;*

    Para desinstalar el archivo DLL, use el siguiente comando de consola:

    **regsvr32.exe** **/u** *&lt; dll name &gt;*

-   Reinicie el servicio EAPHost.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> </dl>

 

 