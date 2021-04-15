---
title: El puerto 3 está en desuso para los controladores NDIS 6,30
description: El puerto 3 está en desuso para los controladores NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488410"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>El puerto 3 está en desuso para los controladores NDIS 6,30

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

Windows 8 quita la compatibilidad de la plataforma para los controladores de WLAN del minipuerto NDIS para crear o iniciar el puerto de extensibilidad de IHV (también conocido como tercer puerto). Esta característica se presentó en Windows 7 como medida provisional mientras que Wi-Fi Alliance (WFA) desarrolló la Wi-Fi especificación directa. La especificación ya ha finalizado, los productos que usan Wi-Fi Direct se están certificando y Windows 8 presenta una pila de Wi-Fi directo nativa.

## <a name="manifestation"></a>Manifestación

Nada, ya que el tercer puerto es una funcionalidad de plataforma en la que se inician los controladores de minipuerto de WLAN si necesitan esta funcionalidad.

## <a name="solution"></a>Solución

Estamos manteniendo la característica de puerto de extensibilidad disponible para los controladores existentes que no informan de NDIS 6,30 para mantener la compatibilidad de los dispositivos. Sin embargo, los nuevos controladores de WLAN que informan de NDIS 6,30 no podrán iniciar este puerto; en su lugar, los desarrolladores de estos controladores deben usar Wi-Fi directo.

 

 




