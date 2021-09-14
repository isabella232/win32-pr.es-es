---
description: Los proveedores de paquetes de red (NPP) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245265"
---
# <a name="npp-interfaces"></a>NPP Interfaces

Los proveedores de paquetes de red (NPP) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red. Al llamar a [CreateNPPInterface](createnppinterface.md), recuerde que cada NPP se representa como un único objeto COM en proceso. Las aplicaciones pueden crear instancias de cualquier número de objetos NPP. Sin embargo, cada objeto con instancias debe usar una (y solo una) de las cinco interfaces NPP.

Tenga en cuenta también que las distintas interfaces NPP proporcionan datos de red de varias formas. Por ejemplo, Monitor de red la **interfaz IDelaydC** para capturar el tráfico de red y guardarlo en un archivo de captura. mientras que los monitores usan **la interfaz IRTC** para capturar el tráfico de red en tiempo real. En la tabla siguiente se Monitor de red interfaces NPP.



| Interfaz                | Descripción                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Captura el tráfico de red que se almacena en un archivo de captura. Esta interfaz la usan las aplicaciones Monitor de red y NPP.                                          |
| [IESP](iesp.md)         | Captura el tráfico de red que se almacena en un archivo de captura y proporciona estadísticas mejoradas en un formato de archivo ESP especial. Esta interfaz la usan las aplicaciones NPP. |
| [IRTC](irtc.md)         | Captura el tráfico de red en tiempo real y desencadena eventos cuando se producen. Esta interfaz la usan [*monitores y*](m.md) aplicaciones NPP.     |
| [IStats](istats.md)     | Recupera las estadísticas como datos sin procesar en lugar de fotogramas. Esta interfaz la usan aplicaciones NPP como [*Perfmon.*](p.md)                     |



 

 

 



