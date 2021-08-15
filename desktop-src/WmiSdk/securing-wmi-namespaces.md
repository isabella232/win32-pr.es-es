---
description: El acceso a los espacios de nombres WMI y sus datos se controla mediante descriptores de seguridad.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Protección de espacios de nombres WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992376"
---
# <a name="securing-wmi-namespaces"></a>Protección de espacios de nombres WMI

El acceso a los espacios de nombres WMI y sus datos se controla mediante [*descriptores de seguridad*](gloss-s.md). Puede proteger los [](gloss-n.md) datos de los espacios de nombres ajustando el descriptor de seguridad del espacio de nombres para controlar quién tiene acceso a los datos y métodos. Para obtener más información, vea [Acceso a objetos protegibles wmi.](access-to-wmi-securable-objects.md)


En los temas siguientes se describe la seguridad del espacio de nombres WMI y cómo controlar el acceso a los espacios de nombres.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dd>

La seguridad del espacio de nombres WMI se basa Windows [*identificadores*](/windows/desktop/SecGloss/s-gly) de seguridad de usuario (SID) y listas de control de acceso estándar. Los administradores y los usuarios tienen permisos predeterminados diferentes.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Establecer descriptores de seguridad de espacio de nombres](setting-namespace-security-descriptors.md)
</dt> <dd>

Una vez que existe un espacio de nombres en el repositorio WMI, puede cambiar la seguridad en el espacio de nombres mediante el control WMI o llamando a los métodos [**\_ \_ de SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

El **calificador RequiresEncryption** en un espacio de nombres requiere que la aplicación cliente WMI o el script usen el nivel de autenticación que cifra las llamadas a procedimiento remoto. Tanto las solicitudes de datos entrantes como las devoluciones de llamada asincrónicas deben cifrarse.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Creación de un espacio de nombres con la API wmi](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
