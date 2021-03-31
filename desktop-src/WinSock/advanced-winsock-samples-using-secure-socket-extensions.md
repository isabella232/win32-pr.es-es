---
description: Ejemplos avanzados de Winsock con extensiones de socket seguras
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Ejemplos avanzados de Winsock con extensiones de socket seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001145"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Ejemplos avanzados de Winsock con extensiones de socket seguras

## <a name="secure-tcp-client-and-server-sample"></a>Ejemplo de cliente y servidor TCP seguro

En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de Winsock más avanzado que muestra el uso de extensiones de sockets seguros. El ejemplo incluye un cliente TCP y un servidor que se conectan de forma segura mediante las extensiones Winsock y socket seguro.

De forma predeterminada, el código fuente de ejemplo de Winsock se instala en el directorio siguiente:

*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ NetDs \\ Winsock*

Un ejemplo se encuentra en la siguiente carpeta:

*securesocket*

El código de ejemplo se divide en directorios independientes, tal y como se describe a continuación:

-   stcpclient: la carpeta que contiene el código de cliente TCP seguro.
-   stcpcommon: la carpeta que contiene el código de biblioteca común que se comparte entre el cliente y el servidor TCP seguros.
-   stcpserver: la carpeta que contiene el código de servidor TCP seguro.

Se debe observar que los ejemplos están diseñados para ejecutarse en dos equipos diferentes que ejecutan Windows Vista o posterior. Además, las credenciales de IPsec se deben aprovisionar en ambos equipos para que la conexión se realice correctamente, ya que el ejemplo utiliza IPsec para proteger su tráfico. Consulte la documentación sobre la [configuración de IPSec](/windows/desktop/FWP/ipsec-configuration) para obtener más información sobre cómo configurar las credenciales de IPSec.

Al compilar el ejemplo se generarán dos archivos ejecutables:

*stcpclient.exe* y *stcpserver.exe*.

Copie *stcpclient.exe* en el equipo a y copie *stcpserver.exe* en el equipo B. En el equipo B, inicie el servidor TCP; para ello, ejecute lo siguiente en un símbolo del sistema:

**stcpserver.exe**

Ejecute el siguiente comando para obtener más opciones de uso para el servidor:

**stcpserver.exe/?**

A continuación, en el equipo A, inicie el cliente TCP ejecutando lo siguiente en un símbolo del sistema:

**stcpclient.exe <DN completo-nombre-de-equipo-B>**

En este momento, la conexión debe establecerse de forma segura.

Ejecute el siguiente comando para obtener más opciones de uso para el cliente:

**stcpclient.exe/?**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la plataforma de filtrado de Windows](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Aplicación del nivel de aplicación (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configuración de IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Funciones de IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Uso de extensiones de socket seguras](using-secure-socket-extensions.md)
</dt> <dt>

[Interfaz del proveedor de compatibilidad con seguridad (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Plataforma de filtrado de Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Funciones de la API de la plataforma de filtrado de Windows](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Extensiones Winsock Secure Socket](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
