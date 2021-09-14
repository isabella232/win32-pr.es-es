---
description: El enrutador de varios proveedores (MPR) controla la comunicación entre el Windows operativo y los proveedores de red instalados. Permite que Windows una red integrada al usuario.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Enrutador de varios proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173425"
---
# <a name="multiple-provider-router"></a>Enrutador de varios proveedores

El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) controla la comunicación entre el Windows operativo y los proveedores de red instalados. Permite que Windows una red integrada al usuario.

Cuando se inicia mpr, comprueba el registro para determinar qué proveedores de red están instalados en el sistema y el orden en el que se deben recorrer. Carga todos los archivos DLL del proveedor de red registrados y los usa para procesar las llamadas WNet posteriores realizadas por la interfaz de usuario u otras aplicaciones.

Para obtener más información sobre las funciones de WNet, [vea Windows Networking](../wnet/windows-networking-wnet-.md).

 

 
