---
title: Adición de la funcionalidad de Microsoft Agent a la aplicación
description: Adición de la funcionalidad de Microsoft Agent a la aplicación
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf604a7e18d67865fb50981833ce808985e455118326c4f157258543e236dd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753134"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Adición de la funcionalidad de Microsoft Agent a la aplicación

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para acceder a las interfaces de servidor de Microsoft Agent, el Agente ya debe estar instalado en el sistema de destino. No se admite la instalación que no sea mediante el archivo ejecutable de instalación automática del Agente, como intentar copiar y registrar archivos de componentes del Agente . Esto garantiza una instalación coherente y completa. Tenga en cuenta que el archivo de instalación propia de Microsoft Agent no se instalará en Microsoft Windows 2000 y sistemas operativos posteriores, ya que estas versiones del sistema operativo ya incluyen su propia versión del Agente .

Para instalar correctamente el Agente en un sistema de destino con un sistema operativo de Microsoft Windows anterior, también debe asegurarse de que el sistema de destino tiene una versión reciente del runtime de Microsoft Visual C++ (Msvcrt.dll), la herramienta de registro de Microsoft (Regsvr32.dll) y los archivos DLL de Microsoft COM. La manera más fácil de asegurarse de que los componentes necesarios están en el sistema de destino es requerir que Microsoft Internet Explorer 3.02 o posterior esté instalado. Como alternativa, puede instalar los dos primeros componentes que están disponibles como parte de Microsoft Visual C++. Los archivos DLL COM necesarios se pueden instalar como parte de la actualización de Microsoft DCOM, disponible en el sitio web de Microsoft. Puede encontrar más información e información de licencias para estos componentes en el sitio web de Microsoft.

Los componentes de lenguaje del agente se pueden instalar de la misma manera. De forma similar, puede usar esta técnica para instalar el formato ACS de los caracteres de Microsoft disponibles para su distribución desde el sitio web de Microsoft Agent. Los archivos de caracteres se instalan automáticamente en el \\ subdirectorio Chars del agente de Microsoft.

Dado que los componentes de Microsoft Agent están diseñados como componentes del sistema operativo, es posible que el Agente no se desinstale. De forma similar, si el Agente ya está instalado como parte del sistema operativo Windows, es posible que el gabinete de instalación automática del Agente no se instale.

Una vez instalado, para llamar a las interfaces del Agente , cree una instancia del servidor y solicite un puntero a una interfaz específica que el servidor admita mediante la convención COM estándar. En concreto, la biblioteca COM proporciona una función de API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), que crea una instancia del objeto y devuelve un puntero a la interfaz solicitada del objeto. Solicite un puntero a la [**interfaz IAgent**](iagent.md) o [**IAgentEx**](iagentex.md) en la **llamada a CoCreateInstance** o en una llamada posterior a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

El código siguiente muestra esto en C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Si el servidor de Microsoft Agent se está ejecutando, esta función se conecta al servidor; De lo contrario, inicia el servidor.

Tenga en cuenta que las interfaces de servidor de Microsoft Agent suelen incluir interfaces extendidas que incluyen un sufijo "Ex". Estas interfaces se derivan de y, por tanto, incluyen toda la funcionalidad de sus homólogos que no son Ex. Si desea usar cualquiera de las características extendidas, use las interfaces Ex.

Las funciones que toman punteros a BSTR asignan memoria [**mediante SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). Es responsabilidad del autor de la llamada liberar esta memoria [**mediante SysFreeString.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

 

 