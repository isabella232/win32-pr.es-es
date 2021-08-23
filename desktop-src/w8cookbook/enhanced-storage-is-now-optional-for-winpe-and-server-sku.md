---
title: El almacenamiento mejorado ahora es opcional para WINPE y la SKU de servidor
description: El almacenamiento mejorado ahora es opcional para WINPE y la SKU de servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028853"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>El almacenamiento mejorado ahora es opcional para WINPE y la SKU de servidor

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

El almacenamiento mejorado siempre estaba disponible en Windows 7 dispositivos USB. Con la versión de Windows 8, está disponible para todos los dispositivos de almacenamiento. En los dispositivos basados en cliente, está habilitado de forma predeterminada; en los dispositivos de servidor es opcional y se debe aprovisionar a través Windows entorno de preinstalación (WinPE).

## <a name="manifestation"></a>Manifestación

Se producirá un error en el dispositivo del servidor si el almacenamiento mejorado no está habilitado.

Los dispositivos de arranque deben aprovisionarse a través de WinPE con esta opción habilitada.

## <a name="solution"></a>Solución

Dado que el almacenamiento mejorado es opcional para el servidor en tiempo de ejecución, los desarrolladores deben agregarlo a WinPE para el aprovisionamiento y la activación de esas unidades. Consulte la guía de implementación para obtener más información.

A continuación, los administradores del servidor deben configurar explícitamente su servidor para usar el almacenamiento mejorado.

 

 




