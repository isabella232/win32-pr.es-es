---
description: A partir de Windows Server 2008, el proveedor de características de servidor proporciona información sobre las características de servidor que están instaladas en el servidor. Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.
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
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706458"
---
# <a name="server-feature-provider"></a>Proveedor de características de servidor

A partir de Windows Server 2008, el proveedor de características de servidor proporciona información sobre las características de servidor que están instaladas en el servidor. Esta clase permite a los administradores inventariar y administrar sus roles y características de servidor.

Un rol de servidor se define como un grupo de componentes que proporcionan funciones para un área específica de funcionalidad, como impresión, archivos, control de dominio, etc. Los roles de servidor típicos son servidor de archivos, servidor de correo, servidor DNS, controlador de dominio, servidor de aplicaciones, etc.

Si una empresa no ejecuta software de administración que informe de roles de servidor, como Microsoft Operations Manager con módulos de administración instalados, puede obtener esa información consultando la clase [**\_ ServerFeature de Win32**](win32-serverfeature.md) . La información de roles de servidor y características de los equipos remotos está disponible a través de las conexiones remotas WMI normales o mediante el servicio Administración remota de Windows (WinRM). Para obtener más información acerca de las conexiones remotas DCOM de WMI, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md). Para obtener más información sobre las conexiones que usan el protocolo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , vea [administración remota de Windows](/windows/desktop/WinRM/portal).

El proveedor de características de servidor de admite las siguientes clases WMI:

-   [**Win32 \_ ServerFeature**](win32-serverfeature.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 
