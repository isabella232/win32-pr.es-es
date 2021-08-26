---
title: Uso de Servicios de Escritorio remoto
description: Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología Servicios de Escritorio remoto (anteriormente conocida como Terminal Services) a la Web mediante Conexión web a Escritorio remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d0af90aef8eed3c8b9dc397f86cb6940a79e8e399af201ff854cbfaba3ff3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868775"
---
# <a name="using-remote-desktop-services"></a>Uso de Servicios de Escritorio remoto

En las secciones siguientes se describe cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología Servicios de Escritorio remoto (anteriormente conocida como Terminal Services) a la web mediante Conexión web a Escritorio remoto. Si busca información de usuario para las conexiones Escritorio remoto, vea Conectar a otro equipo [mediante Conexión a Escritorio remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Este tema está disponible para desarrolladores de software.

 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Detectar si el rol Servicios de Escritorio remoto está instalado](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

Ejemplo de código de C# que muestra un método que devuelve **True** si el rol de servidor Servicios de Escritorio remoto está instalado y en ejecución o **false** en caso contrario, a partir de Windows Server 2008.

</dd> <dt>

[Extensión del Agente de sesión de Terminal Services](extending-ts-session-broker.md)
</dt> <dd>

Puede extender el Agente de sesión de TS mediante la [**interfaz COM de IWTSSBPlugin.**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)

</dd> <dt>

[Implementar un enumerador de extremo de audio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

A partir Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor Escritorio remoto protocolo.

</dd> <dt>

[Monikers de sesión](session-monikers.md)
</dt> <dd>

COM distribuido (DCOM) habilita la activación de objetos por sesión mediante un moniker de sesión proporcionado por el sistema.

</dd> <dt>

[Uso de la extensión ADSI para la Servicios de Escritorio remoto usuario](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante los métodos implementados por la extensión Active Directory Service Interfaces (ADSI), que se empaqueta con la biblioteca de vínculos dinámicos Tsuserex.dll.

</dd> <dt>

[Uso de Servicios de Escritorio remoto API](using-the-terminal-services-api.md)
</dt> <dd>

Describe cómo puede usar la API de Servicios de Escritorio remoto para permitir que las aplicaciones realicen tareas en un Servicios de Escritorio remoto trabajo.

</dd> <dt>

[Uso de Escritorio remoto Virtualization API](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Los desarrolladores pueden usar esta API para personalizar la lógica que Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) para determinar el mejor destino para una conexión de cliente entrante.

</dd> <dt>

[Interfaz WSDL para soluciones de VDI personalizadas](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Los desarrolladores pueden crear servicios web personalizados que administren soluciones de infraestructura de escritorio virtual (VDI).

</dd> </dl>

Para obtener más información, vea [Servicios de Escritorio remoto de programación .](terminal-services-programming-guidelines.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Terminal Services ya está Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Detección del entorno Servicios de Escritorio remoto de datos](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




