---
title: Usar Servicios de Escritorio remoto
description: Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685552"
---
# <a name="using-remote-desktop-services"></a>Usar Servicios de Escritorio remoto

En las secciones siguientes se describe cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto. Si está buscando información de usuario para conexiones Escritorio remoto, consulte [conectarse a otro equipo mediante conexión a escritorio remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Este tema está destinado a los desarrolladores de software.

 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Detectar si está instalado el rol de Servicios de Escritorio remoto](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

Ejemplo de código de C# que muestra un método que devuelve **true** si la función de servidor servicios de escritorio remoto está instalada y en ejecución, o **false** en caso contrario, a partir de Windows Server 2008.

</dd> <dt>

[Extender Terminal Services agente de sesiones](extending-ts-session-broker.md)
</dt> <dd>

Puede extender el agente de sesiones de TS mediante la interfaz com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .

</dd> <dt>

[Implementación de un enumerador de punto de conexión de audio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto.

</dd> <dt>

[Monikers de sesión](session-monikers.md)
</dt> <dd>

COM distribuido (DCOM) permite la activación de objetos por sesión mediante el uso de un moniker de sesión proporcionado por el sistema.

</dd> <dt>

[Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante el uso de los métodos implementados por la extensión de interfaces de servicio Active Directory (ADSI), que se incluye con la biblioteca de vínculos dinámicos Tsuserex.dll.

</dd> <dt>

[Uso de la API de Servicios de Escritorio remoto](using-the-terminal-services-api.md)
</dt> <dd>

Describe cómo puede usar la API de Servicios de Escritorio remoto para permitir que las aplicaciones realicen tareas en un entorno de Servicios de Escritorio remoto.

</dd> <dt>

[Uso de la API de virtualización de Escritorio remoto](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Los desarrolladores pueden usar esta API para personalizar la lógica que usa Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto) para determinar el mejor destino para una conexión de cliente entrante.

</dd> <dt>

[Interfaz WSDL para soluciones VDI personalizadas](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Los desarrolladores pueden crear servicios web personalizados que administren soluciones de infraestructura de escritorio virtual (VDI).

</dd> </dl>

Para obtener más información, vea [instrucciones de programación de servicios de escritorio remoto](terminal-services-programming-guidelines.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Terminal Services es ahora Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Detección del entorno de Servicios de Escritorio remoto](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




