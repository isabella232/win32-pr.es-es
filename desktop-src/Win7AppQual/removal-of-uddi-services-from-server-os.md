---
description: Eliminación de servicios UDDI del sistema operativo del servidor
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Eliminación de servicios UDDI del sistema operativo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242949"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Eliminación de servicios UDDI del sistema operativo del servidor

## <a name="affected-platform"></a>Plataforma afectada

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** baja  

## <a name="description"></a>Descripción

Microsoft ha quitado el rol de servidor udDI (Universal Description, Discovery, and Integration) Services de Windows Server 2008 R2. Las versiones futuras de los servicios UDDI formarán parte del producto de Microsoft BizTalk. Este producto de realineación y consolidación coloca a Microsoft para servir mejor al mercado de arquitectura orientada a servicios (SOA).

La primera versión posterior Windows Server 2008 de los servicios UDDI será compatible con los estándares UDDI v3.0. Se enviará como parte de la versión BizTalk Server 2009. Para cumplir nuestro compromiso de proporcionar una experiencia de usuario satisfactoria, ofreceremos un paquete de instalación de UDDI Services v3 para Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestación

La presencia de versiones anteriores de componentes de servicios UDDI en el sistema bloquea una actualización a Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

Los usuarios que han implementado un sitio de servicios UDDI desde Windows Server 2003 o Windows Server 2008 pueden optar por no actualizar los servidores que ejecutan los servicios UDDI a Windows Server 2008 R2. También pueden mover los servicios UDDI a cuadros dedicados de Windows Server 2003 o Windows Server 2008 si tienen que actualizar los cuadros de servicios UDDI actuales.

## <a name="solution"></a>Solución

La solución recomendada es implementar uddi Services v3.0 desde BizTalk Server 2009 en una máquina de Windows Server 2008 R2 y, a continuación, migrar el sitio antiguo al nuevo sitio. Servicios UDDI v3.0 proporciona compatibilidad con versiones anteriores con UDDI Services 2.0, por lo que las aplicaciones que usen servicios UDDI no se verán afectadas.

Para ello, realice los pasos siguientes:

1.  Configure un nuevo sitio de UDDI Services v3.0 en una máquina ya cargada con Windows Server 2008 R2. (Nota: En una instalación distribuida, un sitio UDDI v3.0 puede constar de más de una máquina Windows Server 2008 R2).
2.  Use la herramienta de migración de datos UDDI para migrar los datos de la base de datos antigua de servicios UDDI a la nueva base de datos.
3.  Realizar una copia de seguridad de la base de datos antigua de servicios UDDI para garantizar la funcionalidad de reversión.
4.  Desinstale el software de servicios UDDI antiguo y, a continuación, actualice esos cuadros a Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Sitio web de servicios UDDI de Microsoft](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Especificaciones de UDDI](http://uddi.xml.org/specification)
-   [Descarga de servicios UDDI v3.0 para Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



