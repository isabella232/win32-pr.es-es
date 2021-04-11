---
description: A partir de Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275934"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partir de Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto. Un administrador puede realizar una instalación desde la sesión de consola de un servidor de Terminal Server. Un administrador también puede realizar una instalación desde una sesión de cliente del servidor de Terminal Server.

Para obtener más información, vea [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) en el kit de desarrollo de software (SDK) de Microsoft Windows.

* * Sistemas operativos anteriores a Windows Server 2008 y Windows Vista: * *

La configuración de esta [Directiva del sistema](system-policy.md) por equipo permite a los administradores realizar instalaciones desde una sesión de cliente del servidor de Terminal Server. Si no se establece esta Directiva, los administradores solo pueden realizar instalaciones desde la sesión de consola. Los usuarios no administrativos nunca pueden realizar instalaciones desde una sesión de cliente. El valor predeterminado de esta directiva permite que solo los administradores realicen instalaciones desde la sesión de consola. Los administradores siempre pueden realizar [instalaciones administrativas](administrative-installation.md) desde una sesión de cliente del servidor de Terminal Server o desde la sesión de consola, independientemente de si esta directiva está establecida.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

Para obtener más información, vea también [usar Windows Installer con un terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
