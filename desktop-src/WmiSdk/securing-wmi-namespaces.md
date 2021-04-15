---
description: Los descriptores de seguridad controlan el acceso a los espacios de nombres de WMI y sus datos.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Proteger los espacios de nombres de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715755"
---
# <a name="securing-wmi-namespaces"></a>Proteger los espacios de nombres de WMI

Los [*descriptores de seguridad*](gloss-s.md)controlan el acceso a los espacios de nombres de WMI y sus datos. Puede proteger los datos de los [*espacios de nombres*](gloss-n.md) ajustando el descriptor de seguridad del espacio de nombres para controlar quién tiene acceso a los datos y métodos. Para obtener más información, vea [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).


En los temas siguientes se describe la seguridad del espacio de nombres WMI y cómo controlar el acceso a los espacios de nombres.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dd>

La seguridad del espacio de nombres WMI se basa en los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) de usuario (SID) y listas de control de acceso estándar de Windows. Los administradores y los usuarios tienen permisos predeterminados diferentes.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md)
</dt> <dd>

Después de que exista un espacio de nombres en el repositorio WMI, puede cambiar la seguridad en el espacio de nombres mediante el control WMI o llamando a los métodos de [**\_ \_ SystemSecurity**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

El calificador **RequiresEncryption** de un espacio de nombres requiere que la aplicación cliente WMI o el script utilicen el nivel de autenticación que cifra las llamadas a procedimiento remoto. Las solicitudes de datos entrantes y las devoluciones de llamada asincrónicas se deben cifrar.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establecer la herencia de la seguridad del espacio de nombres](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Crear un espacio de nombres con la API de WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
