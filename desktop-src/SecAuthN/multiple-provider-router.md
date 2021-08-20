---
description: El enrutador de varios proveedores (MPR) controla la comunicación entre el Windows operativo y los proveedores de red instalados. Permite que Windows una red integrada al usuario.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Enrutador de varios proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786583"
---
# <a name="multiple-provider-router"></a>Enrutador de varios proveedores

El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) controla la comunicación entre el Windows operativo y los proveedores de red instalados. Permite que Windows una red integrada al usuario.

Cuando se inicia MPR, comprueba el registro para determinar qué proveedores de red están instalados en el sistema y el orden por el que se deben recorrer. Carga todos los archivos DLL del proveedor de red registrados y los usa para procesar las llamadas WNet posteriores realizadas por la interfaz de usuario u otras aplicaciones.

Para obtener más información sobre las funciones de WNet, [vea Windows Networking](../wnet/windows-networking-wnet-.md).

 

 
