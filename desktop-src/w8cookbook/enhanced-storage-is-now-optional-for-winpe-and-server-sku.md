---
title: El almacenamiento mejorado ahora es opcional para WINPE y sku de servidor
description: El almacenamiento mejorado ahora es opcional para WINPE y sku de servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575649"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>El almacenamiento mejorado ahora es opcional para WINPE y sku de servidor

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

El almacenamiento mejorado siempre estaba disponible en Windows 7 dispositivos USB. Con el lanzamiento de Windows 8, está disponible para todos los dispositivos de almacenamiento. En los dispositivos basados en cliente, está habilitado de forma predeterminada; en dispositivos de servidor es opcional y se debe aprovisionar mediante Windows de preinstalación (WinPE).

## <a name="manifestation"></a>Manifestación

Se producirá un error en el dispositivo de servidor si el almacenamiento mejorado no está habilitado.

Los dispositivos de arranque se deben aprovisionar a través de WinPE con esta opción habilitada.

## <a name="solution"></a>Solución

Dado que el almacenamiento mejorado es opcional para el servidor en tiempo de ejecución, los desarrolladores deben agregarlo a WinPE para aprovisionar y activar esas unidades. Consulte la guía de implementación para obtener más información.

A continuación, los administradores del servidor deben configurar explícitamente su servidor para que use el almacenamiento mejorado.

 

 




