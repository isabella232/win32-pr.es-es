---
description: En la ilustración siguiente se muestra la relación entre las aplicaciones de expertos y analizadores y otros componentes de Monitor de red arquitectura.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitectura de expertos y analizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261343005f0cb9fc7de5b7025f9ffe59f11515614ab43609c1b8da9f396e9f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795851"
---
# <a name="expert-and-parser-architecture"></a>Arquitectura de expertos y analizadores

En la ilustración siguiente se muestra la [relación](experts.md) entre las [aplicaciones](parsers.md) de expertos y analizadores y otros componentes de Monitor de red arquitectura.

![la relación entre las aplicaciones de expertos y analizadores](images/nm-arch1.png)

El tráfico de red se recopila, como fotogramas individuales, desde el controlador NDIS. El controlador Monitor de red (Nmnt.sys) enruta las tramas a un proveedor de paquetes de red (NPP), que captura los datos y los coloca en uno o varios archivos de captura. El NPP es una colección de interfaces COM que se usan para capturar datos. En este caso, la [**interfaz IDelaydC**](idelaydc.md) se usa para realizar una captura retrasada.

> [!Note]  
> El NPP se usa para las capturas retrasadas y en tiempo real. Para las capturas en tiempo real, se [**usa la interfaz IRTC.**](irtc.md)

 

Cuando los marcos de red se almacenan en el archivo de captura y el archivo es accesible, los expertos y analizadores pueden usar la interfaz de usuario de Monitor de red y las funciones de Monitor de red proporcionadas en Nmapi.dll para analizar los datos. Los archivos de captura no son accesibles hasta que se completa la captura.

 

 



