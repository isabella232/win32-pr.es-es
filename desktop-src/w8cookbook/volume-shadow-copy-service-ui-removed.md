---
title: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
description: Interfaz de usuario de versiones anteriores quitada para volúmenes locales
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b24df290222158d8e26d89603d37364c820fabe732fd8107824d2ef9576d30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706775"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Interfaz de usuario de versiones anteriores quitada para volúmenes locales

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


## <a name="description"></a>Descripción

Las versiones anteriores de Windows permitían a los usuarios restaurar versiones anteriores de archivos individuales a partir de "instantáneas" de volúmenes locales. Estas instantáneas se crean mediante la característica "Versiones anteriores" a través del servicio de instantáneas de volumen (VSS). En Windows 7, los usuarios podían configurar y programar instantáneas en la interfaz de usuario de Protección del sistema disponible a través de Propiedades del sistema.

Sin embargo, las versiones anteriores rara vez se usaron y afectaron negativamente al rendimiento Windows general. como resultado, se quitó la característica. En Windows 8, estas características ya no están disponibles:

-   La capacidad de examinar, buscar o restaurar versiones anteriores de archivos a través de la interfaz de usuario de versiones anteriores
-   La capacidad de configurar o programar versiones anteriores de archivos a través de la interfaz de usuario de Protección del sistema

Sin embargo, los usuarios pueden seguir utilizando la pestaña Versiones anteriores al acceder a recursos compartidos de archivos en Windows servidor.

## <a name="manifestation"></a>Manifestación

La opción Versiones anteriores ya no está disponible para los volúmenes locales en el Windows propiedades del Explorador de aplicaciones.

## <a name="solution"></a>Solución

Los desarrolladores que necesitan crear instantáneas de volúmenes locales pueden seguir llamando a las API de VSS en código personalizado.

 

 




