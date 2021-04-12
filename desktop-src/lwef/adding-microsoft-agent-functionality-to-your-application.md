---
title: Agregar la funcionalidad de Microsoft Agent a la aplicación
description: Agregar la funcionalidad de Microsoft Agent a la aplicación
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358874"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Agregar la funcionalidad de Microsoft Agent a la aplicación

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para tener acceso a las interfaces de servidor de Microsoft Agent, el agente ya debe estar instalado en el sistema de destino. No se admite la instalación que no sea con el archivo ejecutable de instalación automática del agente, como intentar copiar y registrar archivos de componente de agente. Esto garantiza una instalación coherente y completa. Tenga en cuenta que el archivo de instalación automática de Microsoft Agent no se instalará en los sistemas operativos Microsoft Windows 2000 y versiones posteriores, ya que estas versiones del sistema operativo ya incluyen su propia versión del agente.

Para instalar correctamente el agente en un sistema de destino con un sistema operativo Microsoft Windows anterior, también debe asegurarse de que el sistema de destino tiene una versión reciente de Microsoft Visual C++ Runtime (Msvcrt.dll), la herramienta de registro de Microsoft (Regsvr32.dll) y los archivos dll de Microsoft COM. La manera más sencilla de asegurarse de que los componentes necesarios están en el sistema de destino es requerir la instalación de Microsoft Internet Explorer 3,02 o posterior. Como alternativa, puede instalar los dos primeros componentes que están disponibles como parte de Microsoft Visual C++. Los archivos DLL COM necesarios se pueden instalar como parte de la actualización DCOM de Microsoft, disponible en el sitio web de Microsoft. Puede encontrar más información e información de licencia para estos componentes en el sitio web de Microsoft.

Los componentes de idioma del agente se pueden instalar de la misma manera. De forma similar, puede usar esta técnica para instalar el formato de ACS de los caracteres de Microsoft disponibles para la distribución desde el sitio web del agente de Microsoft. Los archivos de caracteres se instalan automáticamente en el subdirectorio de caracteres del agente de Microsoft \\ .

Dado que los componentes de Microsoft Agent están diseñados como componentes del sistema operativo, es posible que el agente no se desinstale. Del mismo modo, si el agente ya está instalado como parte del sistema operativo Windows, es posible que el archivo. cab de instalación automática del agente no se instale.

Una vez instalado, para llamar a las interfaces del agente, cree una instancia del servidor y solicite un puntero a una interfaz específica que el servidor admita mediante la Convención COM estándar. En concreto, la biblioteca COM proporciona una función de API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), que crea una instancia del objeto y devuelve un puntero a la interfaz solicitada del objeto. Solicite un puntero a la interfaz [**IAgent**](iagent.md) o [**IAgentEx**](iagentex.md) en la llamada a **CoCreateInstance** o en una llamada subsiguiente a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

En el código siguiente se muestra esto en C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Si el servidor de agente de Microsoft está ejecutando, esta función se conecta al servidor; de lo contrario, inicia el servidor.

Tenga en cuenta que las interfaces de servidor del agente de Microsoft suelen incluir interfaces extendidas que incluyen un sufijo "ex". Estas interfaces se derivan de y, por tanto, incluyen toda la funcionalidad de, sus homólogos no ex. Si desea utilizar cualquiera de las características extendidas, use las interfaces ex.

Las funciones que toman punteros a BSTR asignan memoria mediante [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). Es responsabilidad del autor de la llamada liberar esta memoria mediante [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring).

 

 