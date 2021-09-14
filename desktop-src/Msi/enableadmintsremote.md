---
description: A partir Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158496"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partir Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto. Un administrador puede realizar una instalación desde la sesión de consola de un servidor de Terminal Server. Un administrador también puede realizar una instalación desde una sesión de cliente del servidor de Terminal Server.

Para más información, consulte [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) en el Kit de desarrollo de software (SDK) de Microsoft Windows.

**Sistemas operativos anteriores a Windows Server 2008 y Windows Vista: **

Al establecer esta directiva de [sistema por](system-policy.md) máquina, los administradores pueden realizar instalaciones desde una sesión de cliente del servidor terminal. Si no se establece esta directiva, los administradores solo pueden realizar instalaciones desde la sesión de consola. Los usuarios no administradores nunca pueden realizar instalaciones desde una sesión de cliente. El valor predeterminado de esta directiva solo permite a los administradores realizar instalaciones desde la sesión de consola. Los administradores siempre pueden realizar [instalaciones administrativas](administrative-installation.md) desde una sesión de cliente del servidor de terminal Server o desde la sesión de consola, independientemente de si se establece esta directiva.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Observaciones

Para obtener más información, vea también [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
