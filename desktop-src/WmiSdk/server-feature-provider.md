---
description: A partir Windows Server 2008, el proveedor de características de servidor proporciona información sobre qué características de servidor están instaladas en el servidor. Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Proveedor de características de servidor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ffdc79b66a51c82f00f2f8079aa332d6e60d2d7cb82b808b6a0ec3ca56c9f93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922983"
---
# <a name="server-feature-provider"></a>Proveedor de características de servidor

A partir Windows Server 2008, el proveedor de características de servidor proporciona información sobre qué características de servidor están instaladas en el servidor. Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.

Un rol de servidor se define como un grupo de componentes que proporcionan funciones para un área específica de funcionalidad, como impresión, archivos, control de dominio, entre otros. Los roles de servidor típicos son Servidor de archivos, Servidor de correo, Servidor DNS, Controlador de dominio, Servidor de aplicaciones, entre otros.

Si una empresa no ejecuta software de administración que notifica roles de servidor, como Microsoft Operations Manager con módulos de administración instalados, puede obtener esa información consultando la clase [**\_ ServerFeature de Win32.**](win32-serverfeature.md) La información de características y roles de servidor de los equipos remotos está disponible a través de conexiones remotas WMI normales o mediante el Windows administración remota (WinRM). Para obtener más información sobre las conexiones DCOM wmi remotas, vea [Conectarse a WMI en un equipo remoto.](connecting-to-wmi-on-a-remote-computer.md) Para obtener más información sobre las conexiones que usan [*el protocolo WS-Management,*](/windows/desktop/WinRM/windows-remote-management-glossary) [vea Windows Administración remota.](/windows/desktop/WinRM/portal)

El proveedor de características de servidor admite las siguientes clases WMI:

-   [**Win32 \_ ServerFeature**](win32-serverfeature.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 
