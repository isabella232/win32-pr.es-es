---
description: Servicios de Escritorio remoto (guía de calidad de Windows Server 2008 R2 y Windows 7 y 2008 R2)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Servicios de Escritorio remoto (guía de calidad de Windows Server 2008 R2 y Windows 7 y 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569740"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Servicios de Escritorio remoto (guía de calidad de Windows Server 2008 R2 y Windows 7 y 2008 R2)

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores:** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descripción

Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permite que varios usuarios simultáneos accedan a Windows Server con el fin de proporcionar servicios de hospedaje de datos y aplicaciones mediante la tecnología "Presentation Virtualization" de Microsoft.

Aunque la mayoría de las aplicaciones de 32 y 64 bits se ejecutan tal y como están en Windows Servicios de Escritorio remoto, otras no tienen el rendimiento esperado debido a la diferencia en la plataforma (entorno de varios usuarios, acceso simultáneo por parte de varios usuarios, etc.).

Para obtener más información sobre la calidad de la aplicación, lea las *white paper application readiness for Terminal Services* (Preparación de la aplicación para Terminal Services). Visite la página Servicios de Escritorio remoto producto y los sitios web de TechNet de TS más información sobre Servicios de Escritorio remoto. Para obtener más información sobre el desarrollo de aplicaciones para Servicios de Escritorio remoto, revise las Instrucciones *de programación de Terminal Services*. (Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones).

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Resistencia de los impactos y sus mitigaciones

Tres cambios en Windows 7 afectan a las aplicaciones en Servicios de Escritorio remoto:

-   Windows Server 2008 R2 es solo de 64 bits
-   Virtualización de IP por sesión
-   Implementaciones basadas en MSI: claves específicas del usuario

**Solo 64 bits Windows Server 2008 R2**

Las aplicaciones escritas para el servidor de 32 bits se ejecutarán en modo WoW y no de forma nativa en Windows Server 2008 R2 o, por lo tanto, en Servicios de Escritorio remoto. Consulte el Windows de solo 7 64 bits para obtener más información.

*Mitigaciones para solo 64 bits Windows Server 2008 R2*

La mayoría de las aplicaciones escritas para 32 bits seguirán funcionando con normalidad en el modo WoW. Las nuevas aplicaciones escritas para Windows 7 Servicios de Escritorio remoto deben desarrollarse y probarse para su implementación en plataformas de 64 bits.

**Virtualización de IP**

Virtualización de IP de Escritorio remoto permite al usuario asignar direcciones IP a las conexiones de Escritorio remoto por sesión o por programa:

-   Si asigna direcciones IP por sesión, todas las aplicaciones usarán la dirección IP de la sesión.
-   Si asigna direcciones IP por programa, solo las aplicaciones especificadas usarán la dirección IP de la sesión y las aplicaciones restantes de la sesión no se verán afectadas.
-   Si asigna direcciones IP para varios programas, compartirán una dirección IP de sesión.
-   Si tiene más de un adaptador de red en el equipo, también debe elegir uno de ellos para Virtualización de IP de Escritorio remoto.

*Mitigaciones de virtualización de IP*

Algunos programas requieren una dirección IP única para cada instancia de la aplicación. Antes de Windows Server 2008 R2, todas las sesiones de un servidor de Escritorio remoto compartían la misma dirección IP, lo que provocaba problemas de compatibilidad para estas aplicaciones. Virtualización de IP de Escritorio remoto permite que estas aplicaciones se ejecuten en un Escritorio remoto Server.

**Implementaciones basadas en MSI**

Compatibilidad con RDS de Microsoft Installer es una nueva característica incluida con Servicios de Escritorio remoto en Windows Server 2008 R2. Con Servicios de Escritorio remoto en Windows Server 2008 R2, el servidor de Escritorio remoto pone en cola las instalaciones de aplicaciones por usuario y, a continuación, las administra Microsoft Installer.

En Windows Server 2008 R2, puede instalar un programa en Escritorio remoto Server igual que instalaría el programa en un escritorio local. Sin embargo, asegúrese de instalar el programa para todos los usuarios e instalar todos los componentes del programa localmente en Escritorio remoto Server.

*Mitigaciones para implementaciones basadas en MSI*

Antes de la versión Windows Server 2008 R2 de Servicios de Escritorio remoto, Windows solo se admite una instalación Windows Installer a la vez. Para las aplicaciones que requerían configuraciones por usuario, como Microsoft Office Word, un administrador necesitaba instalar previamente la aplicación y los desarrolladores de aplicaciones necesitaban probar estas aplicaciones tanto en el cliente de escritorio remoto como en el host de sesión de Escritorio remoto. Windows La característica de compatibilidad de RDS del instalador permite identificar e instalar configuraciones por usuario que faltan para varios usuarios simultáneamente y hace que la experiencia de instalación de la aplicación en Escritorio remoto Server sea similar a la de un escritorio local.

**Windows Server 2008 R2 con el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No se admite. Se produce un error en una instalación de varios paquetes mediante la tabla [MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) [si el Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) rol está habilitado.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Instrucciones de programación de Terminal Services](../termserv/terminal-services-programming-guidelines.md)
-   [Página principal del producto Terminal Services](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Documento técnico sobre preparación de la aplicación para Terminal Services](/collaborate/connect-redirect)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
