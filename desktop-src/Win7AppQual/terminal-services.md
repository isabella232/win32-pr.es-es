---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servicios de Escritorio remoto (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717446"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Servicios de Escritorio remoto (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores** : windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descripción

Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permite que varios usuarios simultáneos obtengan acceso a Windows Server para proporcionar servicios de hospedaje de aplicaciones y datos mediante la tecnología de "virtualización de presentación" de Microsoft.

Aunque la mayoría de las aplicaciones de 32 y 64 bits se ejecutan tal cual en Windows Servicios de Escritorio remoto, algunas otras no funcionan según lo esperado debido a la diferencia en la plataforma (entorno multiusuario, acceso simultáneo de varios usuarios, etc.).

Para obtener más información sobre la calidad de la aplicación, consulte las notas del producto sobre la *preparación de la aplicación para Terminal Services* . Visite la página del Servicios de Escritorio remoto de productos y los sitios web TechNet de TS más información sobre Servicios de Escritorio remoto. Para obtener más información sobre el desarrollo de aplicaciones para Servicios de Escritorio remoto, revise las *instrucciones de programación de Terminal Services*. (Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones).

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Manifiesto de impactos y sus mitigaciones

Tres cambios en Windows 7 afectan a las aplicaciones en Servicios de Escritorio remoto:

-   Windows Server 2008 R2 es solo de 64 bits
-   Virtualización de IP por sesión
-   Implementaciones basadas en MSI: claves específicas del usuario

**64 solo bits de Windows Server 2008 R2**

Las aplicaciones escritas para el servidor de 32 bits se ejecutarán en modo WoW y no de forma nativa en Windows Server 2008 R2 o, por lo tanto, en Servicios de Escritorio remoto. Para obtener más información, vea el tema Windows 7 64-bit only.

*Mitigaciones solo para Windows Server 2008 R2 de 64 bits*

La mayoría de las aplicaciones escritas para 32 bits seguirán funcionando de la forma habitual en el modo WoW. Todas las aplicaciones nuevas escritas para Windows 7 Servicios de Escritorio remoto deben desarrollarse y probarse para su implementación en plataformas de 64 bits.

**Virtualización de IP**

Virtualización de IP de Escritorio remoto permite al usuario asignar direcciones IP a las conexiones de escritorio remoto por sesión o por programa:

-   Si asigna direcciones IP por sesión, todas las aplicaciones usarán la dirección IP de sesión.
-   Si asigna direcciones IP por programa, solo las aplicaciones especificadas usarán la dirección IP de sesión y las demás aplicaciones de la sesión no se verán afectadas.
-   Si asigna direcciones IP para varios programas, compartirán una dirección IP de sesión.
-   Si tiene más de un adaptador de red en el equipo, también debe elegir uno de ellos para Virtualización de IP de Escritorio remoto.

*Mitigaciones para la virtualización de IP*

Algunos programas requieren una dirección IP única para cada instancia de la aplicación. Antes de Windows Server 2008 R2, todas las sesiones de un servidor de escritorio remoto compartían la misma dirección IP, lo que da lugar a problemas de compatibilidad para estas aplicaciones. Virtualización de IP de Escritorio remoto permite que estas aplicaciones se ejecuten en un servidor de Escritorio remoto.

**Implementaciones basadas en MSI**

Compatibilidad de RDS de Microsoft Installer es una característica nueva incluida en Servicios de Escritorio remoto en Windows Server 2008 R2. Con Servicios de Escritorio remoto en Windows Server 2008 R2, las instalaciones de aplicaciones por usuario las pone en cola el servidor de Escritorio remoto y, a continuación, las controla el instalador de Microsoft.

En Windows Server 2008 R2, puede instalar un programa en el servidor de Escritorio remoto de la misma forma que lo haría en un escritorio local. Sin embargo, asegúrese de instalar el programa para todos los usuarios e instalar todos los componentes del programa localmente en el servidor de Escritorio remoto.

*Mitigaciones para implementaciones basadas en MSI*

Antes de la versión de Windows Server 2008 R2 de Servicios de Escritorio remoto, Windows solo admitía una instalación de Windows Installer a la vez. En el caso de las aplicaciones que requieren configuraciones por usuario, como Microsoft Office Word, un administrador necesitaba preinstalar la aplicación y los desarrolladores de aplicaciones necesitaban probar estas aplicaciones en el cliente de escritorio remoto y en el host de sesión de Escritorio remoto. Windows Installer característica compatibilidad de RDS permite identificar e instalar configuraciones por usuario que faltan para varios usuarios simultáneamente y hace que la experiencia de instalación de la aplicación en Escritorio remoto servidor sea similar a la de un escritorio local.

**Windows Server 2008 R2 con el rol de [servicios de escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No compatible. Se produce un error en una instalación de varios paquetes mediante la [tabla MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) si está habilitado el rol [servicios de escritorio remoto](../termserv/terminal-services-portal.md) .

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Instrucciones de programación de Terminal Services](../termserv/terminal-services-programming-guidelines.md)
-   [Terminal Services Página principal del producto](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Preparación de la aplicación para Terminal Services notas del producto](/collaborate/connect-redirect)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
