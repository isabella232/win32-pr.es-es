---
title: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
description: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488406"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Interfaz de usuario de versiones anteriores quitada para volúmenes locales

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


## <a name="description"></a>Descripción

Las versiones anteriores de Windows permitían a los usuarios restaurar versiones anteriores de archivos individuales desde "instantáneas" de volúmenes locales. Estas instantáneas se crean mediante la característica "versiones anteriores" a través del servicio de instantáneas de volumen (VSS). En Windows 7, los usuarios pueden configurar y programar instantáneas en la interfaz de usuario de protección del sistema disponible a través de las propiedades del sistema.

Sin embargo, las versiones anteriores se usaban con poca frecuencia y afectaban negativamente al rendimiento general de Windows; como resultado, se ha quitado la característica. En Windows 8, estas características ya no están disponibles:

-   La capacidad de examinar, buscar o restaurar versiones anteriores de archivos a través de la interfaz de usuario de versiones anteriores
-   La capacidad de configurar o programar versiones anteriores de archivos a través de la interfaz de usuario de protección del sistema

Sin embargo, los usuarios pueden seguir usando la pestaña versiones anteriores al obtener acceso a recursos compartidos de archivos en un servidor Windows.

## <a name="manifestation"></a>Manifestación

La opción versiones anteriores ya no está disponible para los volúmenes locales en el menú propiedades del explorador de Windows.

## <a name="solution"></a>Solución

Los desarrolladores que necesitan crear instantáneas de volúmenes locales pueden hacerlo mediante una llamada a las API de VSS en código personalizado.

 

 




