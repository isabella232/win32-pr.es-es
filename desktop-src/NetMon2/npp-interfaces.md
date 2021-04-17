---
description: Los proveedores de paquetes de red (NPPs) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666671"
---
# <a name="npp-interfaces"></a>Interfaces NPP

Los proveedores de paquetes de red (NPPs) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red. Cuando llame a [CreateNPPInterface](createnppinterface.md), recuerde que cada NPP se representa como un único objeto com en proceso. Las aplicaciones pueden crear instancias de cualquier número de objetos NPP. Sin embargo, cada objeto con instancias debe usar uno, y solo uno, de las cinco interfaces NPP.

Tenga en cuenta también que diferentes interfaces NPP proporcionan datos de red en varios formatos. Por ejemplo, Monitor de red usa la interfaz **IDelaydC** para capturar el tráfico de red y guardarlo en un archivo de captura; mientras los monitores usan la interfaz **IRTC** para capturar el tráfico de red en tiempo real. En la tabla siguiente se describen Monitor de red interfaces NPP.



| Interfaz                | Descripción                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Captura el tráfico de red que se almacena en un archivo de captura. Esta interfaz la usan las aplicaciones Monitor de red y NPP.                                          |
| [IESP](iesp.md)         | Captura el tráfico de red que se almacena en un archivo de captura y proporciona estadísticas mejoradas en un formato de archivo ESP especial. Esta interfaz la usan las aplicaciones NPP |
| [IRTC](irtc.md)         | Captura el tráfico de red en tiempo real y desencadena eventos cuando se producen. Esta interfaz la usan las aplicaciones de [*monitores*](m.md) y NPP.     |
| [IStas](istats.md)     | Recupera estadísticas como datos sin procesar en lugar de fotogramas. Las aplicaciones NPP, como [*Perfmon*](p.md), usan esta interfaz.                     |



 

 

 



