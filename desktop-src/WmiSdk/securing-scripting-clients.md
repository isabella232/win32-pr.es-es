---
description: Los scripts y las aplicaciones Visual Basic deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y también pueden tener que habilitar los privilegios.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protección de los clientes de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276134"
---
# <a name="securing-scripting-clients"></a>Protección de los clientes de scripting

Los scripts y las aplicaciones Visual Basic deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y también pueden tener que habilitar los privilegios.

## <a name="default-access-permissions"></a>Permisos de acceso predeterminados

El acceso a WMI difiere entre equipos locales y remotos. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

A continuación se muestran los permisos de acceso predeterminados por cuenta:

-   Todos, LocalService, NetworkService

    Permiso para leer o escribir datos y para ejecutar [*métodos de proveedor*](gloss-p.md) en el equipo local. Estas cuentas no pueden crear nuevas clases ni instalar nuevos proveedores.

-   Cuentas de administrador

    Control total en el equipo local. Al conectarse a un equipo remoto, la cuenta también debe ser un administrador local en el equipo remoto.

## <a name="securing-a-scripting-client"></a>Protección de un cliente de scripting

Las aplicaciones de scripting y Visual Basic de WMI deben establecer los niveles de seguridad de DCOM para los sistemas operativos que tienen como destino. Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

Al conectarse a un equipo remoto, es posible que tenga que cambiar el servicio (NTLM o Kerberos) que controla la autenticación. Para obtener más información, vea [establecer el servicio de autenticación con VBScript](setting-the-authentication-service-using-vbscript.md).

El acceso a algunos datos o clases WMI puede requerir un privilegio que no está habilitado. Por ejemplo, debe incluir el privilegio de seguridad al conectarse a la [**clase \_ NTEventlogFile de Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) . Para obtener más información, vea [ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).

Si está accediendo a WMI desde una página de Active Server (ASP), se requiere cierta configuración de IIS. Para obtener más información, vea [configurar IIS 5,0 y versiones posteriores para el scripting de ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md).

Es posible que intente conectarse a un espacio de nombres que requiera una conexión cifrada, es decir, una que requiera un nivel de autenticación de pktPrivacy. Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
