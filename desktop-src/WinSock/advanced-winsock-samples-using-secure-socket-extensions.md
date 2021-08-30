---
description: Ejemplos avanzados de Winsock con extensiones de sockets seguros
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Ejemplos avanzados de Winsock con extensiones de sockets seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477ae91194ef09469cfd857ac36aebabbd4d0f53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886229"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Ejemplos avanzados de Winsock con extensiones de sockets seguros

## <a name="secure-tcp-client-and-server-sample"></a>Ejemplo de cliente y servidor TCP seguro

Un ejemplo de Winsock más avanzado que muestra el uso de extensiones de sockets seguros se incluye con el Kit de desarrollo de software (SDK) de Microsoft Windows. El ejemplo incluye un cliente TCP y un servidor que se conectan de forma segura mediante winsock y las extensiones de socket seguro.

De forma predeterminada, el código fuente de ejemplo winsock se instala en el directorio siguiente:

*C: \\ Archivos de programa Sdk de Microsoft Windows \\ \\ \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Un ejemplo se encuentra en la carpeta siguiente:

*securesocket*

El código de ejemplo se divide en directorios independientes, como se describe a continuación:

-   stcpclient: la carpeta que contiene el código de cliente TCP seguro.
-   stcpcommon: la carpeta que contiene código de biblioteca común que se comparte entre el cliente TCP seguro y el servidor.
-   stcpserver: la carpeta que contiene el código de servidor TCP seguro.

Debe tenerse en cuenta que los ejemplos están diseñados para ejecutarse en dos equipos diferentes que ejecutan Windows Vista o posterior. Además, las credenciales de IPsec deben aprovisionarse en ambos equipos para que la conexión se haga correctamente, ya que en el ejemplo se usa IPsec para proteger su tráfico. Consulte la documentación sobre la configuración [de IPsec](/windows/desktop/FWP/ipsec-configuration) para obtener más información sobre cómo configurar las credenciales de IPsec.

La creación del ejemplo generará dos archivos ejecutables:

*stcpclient.exe* y *stcpserver.exe*.

Copie *stcpclient.exe* en el equipo A y *stcpserver.exe* en el equipo B. En el equipo B, inicie el servidor TCP ejecutando lo siguiente en un símbolo del sistema:

**stcpserver.exe**

Ejecute el siguiente comando para obtener más opciones de uso para el servidor:

**stcpserver.exe /?**

A continuación, en el equipo A, inicie el cliente TCP ejecutando lo siguiente en un símbolo del sistema:

**stcpclient.exe &lt; completo-DNS-name-for-machine-B&gt;**

En este momento, la conexión debe establecerse de forma segura.

Ejecute el siguiente comando para obtener más opciones de uso para el cliente:

**stcpclient.exe /?**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows de filtrado de datos](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Aplicación de la capa de aplicación (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configuración de IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Funciones de IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Uso de extensiones de sockets seguros](using-secure-socket-extensions.md)
</dt> <dt>

[Interfaz del proveedor de compatibilidad con seguridad (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Plataforma de filtrado de Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows Filtrado de funciones de API de plataforma](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Extensiones de socket seguro de Winsock](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
