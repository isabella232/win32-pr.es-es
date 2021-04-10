---
description: En la siguiente ilustración se muestra la relación entre las aplicaciones de experto y de analizador y otros componentes de la arquitectura de Monitor de red.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitectura de expertos y del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153868"
---
# <a name="expert-and-parser-architecture"></a>Arquitectura de expertos y del analizador

En la siguiente ilustración se muestra la relación entre las aplicaciones de [experto](experts.md) y de [analizador](parsers.md) y otros componentes de la arquitectura de monitor de red.

![la relación entre las aplicaciones de expertos y de analizador](images/nm-arch1.png)

El tráfico de red se recopila como fotogramas individuales del controlador NDIS. A continuación, el controlador de Monitor de red (Nmnt.sys) enruta los fotogramas a un proveedor de paquetes de red (NPP), que captura los datos y los coloca en uno o varios archivos de captura. NPP es una colección de interfaces COM que se utiliza para capturar datos. En este caso, la interfaz [**IDelaydC**](idelaydc.md) se utiliza para realizar una captura diferida.

> [!Note]  
> El NPP se utiliza para las capturas retrasadas y en tiempo real. En el caso de las capturas en tiempo real, se usa la interfaz [**IRTC**](irtc.md) .

 

Cuando los fotogramas de red se almacenan en el archivo de captura y se puede tener acceso al archivo, los expertos y analizadores pueden usar la interfaz de usuario de Monitor de red y las funciones de Monitor de red proporcionadas en Nmapi.dll para analizar los datos. No se puede acceder a los archivos de captura hasta que se complete la captura.

 

 



