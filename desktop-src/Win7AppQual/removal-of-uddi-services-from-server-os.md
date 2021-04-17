---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Eliminación de servicios UDDI del sistema operativo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653011"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Eliminación de servicios UDDI del sistema operativo del servidor

## <a name="affected-platform"></a>Plataforma afectada

**Servidores** : Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : baja  

## <a name="description"></a>Descripción

Microsoft ha quitado la función de servidor de servicios UDDI (Universal Description, Discovery, and Integration) de Windows Server 2008 R2. Las versiones futuras de los servicios UDDI formarán parte del producto de Microsoft BizTalk. Esta realineación del producto y la consolidación sitúa a Microsoft para ofrecer un mejor servicio al mercado de la arquitectura orientada a servicios (SOA).

La primera versión posterior a Windows Server 2008 de servicios UDDI será compatible con los estándares de UDDI v 3.0. Se incluirá como parte de la versión BizTalk Server 2009. Para cumplir nuestro compromiso de proporcionar una experiencia de usuario satisfactoria, ofreceremos un paquete de instalación de servicios UDDI v3 para Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestación

La presencia de versiones anteriores de los componentes de servicios UDDI en el sistema bloquea una actualización a Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

Los usuarios que han implementado un sitio de servicios UDDI desde Windows Server 2003 o Windows Server 2008 pueden optar por no actualizar los servidores que ejecutan los servicios UDDI a Windows Server 2008 R2. También pueden trasladar los servicios UDDI a cuadros Windows Server 2003 o Windows Server 2008 dedicados si tienen que actualizar los cuadros de servicios UDDI actuales.

## <a name="solution"></a>Solución

La solución recomendada es implementar los servicios UDDI v 3.0 desde BizTalk Server 2009 en un equipo con Windows Server 2008 R2 y, a continuación, migrar el sitio anterior al nuevo sitio. Servicios UDDI v 3.0 proporciona compatibilidad con versiones anteriores de los servicios UDDI 2,0, por lo que las aplicaciones que usen servicios UDDI no se verán afectadas.

Para ello, siga estos pasos:

1.  Configure un nuevo sitio de servicios UDDI 3.0 en un equipo ya cargado con Windows Server 2008 R2. (Nota: en una instalación distribuida, un sitio UDDI v 3.0 puede constar de más de una máquina con Windows Server 2008 R2).
2.  Use la herramienta de migración de datos UDDI para migrar los datos de la antigua base de datos de servicios UDDI a la nueva base de datos.
3.  Realice una copia de seguridad de la antigua base de datos de servicios UDDI para garantizar la capacidad de reversión.
4.  Desinstale el antiguo software de servicios UDDI y, a continuación, actualice esas casillas a Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Sitio web de servicios UDDI de Microsoft](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Especificaciones de UDDI](http://uddi.xml.org/specification)
-   [Descarga de servicios UDDI v 3.0 para Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



