---
description: Las herramientas de desarrollo de WSDAPI incluidas en el Windows SDK (la CodeGen de WSD, el host de depuración WSD y el cliente de depuración WSD) permiten a los desarrolladores crear y depurar clientes y dispositivos basados en WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Herramientas de desarrollo de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706025"
---
# <a name="wsdapi-development-tools"></a>Herramientas de desarrollo de WSDAPI

Las herramientas de desarrollo de WSDAPI incluidas en el Windows SDK (la CodeGen de WSD, el host de depuración WSD y el cliente de depuración WSD) permiten a los desarrolladores crear y depurar clientes y dispositivos basados en WSDAPI. El código fuente de estas herramientas no está disponible. Las herramientas del SDK se encuentran en el siguiente directorio: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) convierte un contrato WSDL en código C++ generado, al que los desarrolladores pueden llamar directamente. Controla la serialización de datos y la representación de conexión para que los desarrolladores puedan centrarse en el diseño de aplicaciones. Para obtener más información sobre WSD CodeGen, consulte [servicios web en el generador de código de dispositivos](web-services-for-devices-code-generator.md). Esta herramienta está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows y en el kit de controladores de Windows (WDK).

Las herramientas host de depuración WSD (wsddebug \_host.exe) y cliente de depuración WSD (wsddebug \_client.exe) ayudan a los desarrolladores a depurar sus clientes y hosts. Estas herramientas se pueden usar para comprobar e inspeccionar el tráfico de intercambio de metadatos y WS-Discovery. Para obtener más información sobre el host de depuración WSD y el cliente de depuración WSD, vea [herramientas de depuración](debugging-tools.md). Estas herramientas solo están disponibles en el Windows SDK.

Hay una herramienta de desarrollo adicional, denominada [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), que solo está disponible en el WDK. Esta herramienta se utiliza para probar los métodos de servicio, el mecanismo de optimización de transmisión de mensajes (MTOM), los datos adjuntos o WS-Eventing.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Generador de código de servicios web en dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Herramientas de depuración](debugging-tools.md)
</dt> </dl>

 

 



