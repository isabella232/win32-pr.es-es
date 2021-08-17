---
description: A partir Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a644e6f0cb9200fd8a130a2cdb293e7658e3354b817f7378571fae0ab3b4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637109"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partir Windows Server 2008 y Windows Vista, esta directiva ya no tiene ningún efecto. Un administrador puede realizar una instalación desde la sesión de consola de un servidor de Terminal Server. Un administrador también puede realizar una instalación desde una sesión de cliente del servidor terminal.

Para obtener más información, [vea Terminal Services](/windows/desktop/TermServ/terminal-services-portal) en Microsoft Windows Software Development Kit (SDK).

**Sistemas operativos anteriores a Windows Server 2008 y Windows Vista: **

Establecer esta directiva de sistema [por](system-policy.md) máquina permite a los administradores realizar instalaciones desde una sesión de cliente del servidor terminal. Si no se establece esta directiva, los administradores solo pueden realizar instalaciones desde la sesión de consola. Los usuarios no administradores nunca pueden realizar instalaciones desde una sesión de cliente. El valor predeterminado de esta directiva solo permite a los administradores realizar instalaciones desde la sesión de consola. Los administradores siempre pueden realizar instalaciones [administrativas](administrative-installation.md) desde una sesión de cliente del servidor terminal o desde la sesión de consola, independientemente de si se establece esta directiva.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Comentarios

Para obtener más información, vea también Using [Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
