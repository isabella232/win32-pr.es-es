---
title: El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor
description: El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104359461"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>El almacenamiento mejorado ahora es opcional para WINPE y SKU de servidor

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

El almacenamiento mejorado siempre estaba disponible en dispositivos USB de Windows 7. Con el lanzamiento de Windows 8, está disponible para todos los dispositivos de almacenamiento. En los dispositivos basados en cliente, está habilitado de forma predeterminada. en los dispositivos de servidor es opcional y se debe aprovisionar a través de Entorno de preinstalación de Windows (WinPE).

## <a name="manifestation"></a>Manifestación

El dispositivo de servidor producirá un error si el almacenamiento mejorado no está habilitado.

Los dispositivos de arranque deben aprovisionarse a través de WinPE con esta opción habilitada.

## <a name="solution"></a>Solución

Dado que el almacenamiento mejorado es opcional para el servidor en tiempo de ejecución, los desarrolladores deben agregarlo a WinPE para aprovisionar y activar dichas unidades. Consulte la guía de implementación para obtener más información.

Los administradores del servidor deben configurar explícitamente su servidor para que use el almacenamiento mejorado.

 

 




