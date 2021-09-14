---
description: Los scripts Visual Basic aplicaciones deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y es posible que también necesiten habilitar privilegios.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protección de clientes de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967128"
---
# <a name="securing-scripting-clients"></a>Protección de clientes de scripting

Los scripts Visual Basic aplicaciones deben establecer la seguridad de DCOM, especialmente para el acceso remoto, y es posible que también necesiten habilitar privilegios.

## <a name="default-access-permissions"></a>Permisos de acceso predeterminados

El acceso WMI difiere entre equipos locales y remotos. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Estos son los permisos de acceso predeterminados por cuenta:

-   Todos, LocalService, NetworkService

    Permiso para leer o escribir datos y para ejecutar [*métodos de proveedor*](gloss-p.md) en el equipo local. Estas cuentas no pueden crear clases nuevas ni instalar nuevos proveedores.

-   Cuentas de administrador

    Control total en el equipo local. Al conectarse a un equipo remoto, la cuenta también debe ser un administrador local en el equipo remoto.

## <a name="securing-a-scripting-client"></a>Protección de un cliente de scripting

Las aplicaciones de scripting Visual Basic WMI deben establecer los niveles de seguridad de DCOM adecuadamente para los sistemas operativos a los que están destinadas. Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

Al conectarse a un equipo remoto, es posible que tenga que cambiar el servicio (NTLM o Kerberos) que controla la autenticación. Para obtener más información, vea [Establecer el servicio de autenticación mediante VBScript.](setting-the-authentication-service-using-vbscript.md)

El acceso a algunas clases o datos WMI puede requerir un privilegio que no está habilitado. Por ejemplo, debe incluir el privilegio Seguridad al conectarse a la clase [**\_ NTEventlogFile de Win32.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) Para obtener más información, [vea Ejecutar operaciones con privilegios mediante VBScript.](executing-privileged-operations-using-vbscript.md)

Si está accediendo a WMI desde Active Server (ASP), se requiere alguna configuración de IIS. Para obtener más información, vea [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).

Es posible que esté intentando conectarse a un espacio de nombres que requiere una conexión cifrada, es decir, una que requiere un nivel de autenticación de pktPrivacy. Para obtener más información, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

 

 
