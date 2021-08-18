---
description: Las herramientas de desarrollo de WSDAPI incluidas en el SDK de Windows (WSD CodeGen, host de depuración de WSD y cliente de depuración de WSD) permiten a los desarrolladores crear y depurar dispositivos y clientes basados en WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Herramientas de desarrollo de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdad2d87ffafc337c98743f67ae022eb4d1d11616ac42940157a5785066645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130587"
---
# <a name="wsdapi-development-tools"></a>Herramientas de desarrollo de WSDAPI

Las herramientas de desarrollo de WSDAPI incluidas en el SDK de Windows (WSD CodeGen, host de depuración de WSD y cliente de depuración de WSD) permiten a los desarrolladores crear y depurar dispositivos y clientes basados en WSDAPI. El código fuente de estas herramientas no está disponible. Las herramientas del SDK se encuentran en el directorio siguiente: <Windows SDK Install Folder> \\ Bin.

CodeGen de WSD (wsdcodegen.exe) convierte un contrato WSDL en código C++ generado, al que los desarrolladores pueden llamar directamente. Controla la serialización de datos y la representación de conexión para que los desarrolladores puedan centrarse en el diseño de aplicaciones. Para obtener más información sobre WSD CodeGen, vea [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md). Esta herramienta está disponible en microsoft Windows Software Development Kit (SDK) y en Windows Driver Kit (WDK).

Las herramientas WSD Debug Host (wsddebughost.exe) y \_ WSD Debug Client (wsddebugclient.exe) ayudan a los desarrolladores a depurar sus clientes y \_ hosts. Estas herramientas se pueden usar para comprobar e inspeccionar el tráfico WS-Discovery de intercambio de metadatos. Para obtener más información sobre el host de depuración de WSD y el cliente de depuración de WSD, vea [Herramientas de depuración](debugging-tools.md). Estas herramientas solo están disponibles en el SDK Windows.

Hay una herramienta de desarrollo adicional, denominada [WSDAPI Basic Interoperability Tool (WSDBIT),](https://msdn.microsoft.com/library/cc264250.aspx)que solo está disponible en WDK. Esta herramienta se usa para probar métodos de servicio, mecanismo de optimización de transmisión de mensajes (MTOM), datos adjuntos o WS-Eventing.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Generador de código de Servicios web en dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Herramientas de depuración](debugging-tools.md)
</dt> </dl>

 

 



