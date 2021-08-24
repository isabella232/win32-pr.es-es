---
description: Tanto las aplicaciones de C++ como los scripts que se ejecutan con una cuenta de administrador completa pueden cambiar un descriptor de seguridad de espacio de nombres.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Establecer descriptores de seguridad de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc112376a960c3760bc51450cc30b8da3a38c24fa52e985321b2662ae319a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050303"
---
# <a name="setting-namespace-security-descriptors"></a>Establecer descriptores de seguridad de espacio de nombres

Tanto las aplicaciones de C++ como los scripts que se ejecutan con una cuenta de administrador completa pueden cambiar un descriptor de seguridad de espacio de nombres.

## <a name="namespace-security-descriptors"></a>Descriptores de seguridad de espacio de nombres

Cada espacio de nombres WMI tiene un [*descriptor*](/windows/desktop/SecGloss/s-gly)de seguridad , que permite que cada espacio de nombres tenga una configuración de seguridad única que determine quién tiene acceso a los datos y métodos del espacio de nombres. Para obtener más información sobre la seguridad de acceso WMI, vea [Acceso a objetos protegibles de WMI.](access-to-wmi-securable-objects.md) [Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md) describe la configuración de seguridad predeterminada para los espacios de nombres WMI y la auditoría de seguridad en WMI.

Puede establecer permisos de cuenta para cada espacio de nombres WMI en el repositorio WMI (CIM) de las maneras siguientes:

-   Cuando se crea el espacio de nombres en el archivo MOF. Para obtener más información, vea [Establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).
-   Manualmente, mediante el control WMI. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).
-   Mediante programación, llamando a los métodos de la [**\_ \_ clase SystemSecurity.**](--systemsecurity.md)

Los métodos siguientes del [**\_ \_ objeto SystemSecurity**](--systemsecurity.md) asociado a cada espacio de nombres permiten leer o cambiar la seguridad en un espacio de nombres.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Establece el *parámetro rights* como un mapa de bits con cada bit correspondiente a un derecho de acceso.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

Obtiene el descriptor de seguridad del espacio de nombres al que está conectado el usuario. Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes. Si va a escribir un script, use el [**método GetSecurityDescriptor.**](getsecuritydescriptor-method-in-class---systemsecurity-.md)

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

Establece el descriptor de seguridad (SD) del espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si va a escribir un script, use el [**método SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md)

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI asociado a la instancia [**\_ \_ de SystemSecurity**](--systemsecurity.md). El descriptor de seguridad se devuelve como una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora. El descriptor de seguridad se representa mediante una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de Windows descriptores de seguridad no está disponible.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de Windows descriptores de seguridad no está disponible.

</dd> </dl>

Si va a escribir scripts, use [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) y [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md). Puede usar los métodos de la [**clase \_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para modificar los descriptores de seguridad.

Si está programando en C++, puede manipular el descriptor de seguridad binario mediante el Lenguaje de definición de descriptores de seguridad [(SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Tenga en cuenta que, a partir de Windows Vista, el [control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) de cuentas de usuario (UAC) afecta al acceso a los datos WMI y a lo que se puede configurar con el [*control WMI*](gloss-w.md). Para obtener más información, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de seguridad wmi](wmi-security-constants.md)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
