---
description: El enrutador de varios proveedores (MPR) controla la comunicación entre el sistema operativo Windows y los proveedores de red instalados. Permite a Windows presentar al usuario una red integrada.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Enrutador de varios proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911865"
---
# <a name="multiple-provider-router"></a>Enrutador de varios proveedores

El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) controla la comunicación entre el sistema operativo Windows y los proveedores de red instalados. Permite a Windows presentar al usuario una red integrada.

Cuando se inicia el MPR, comprueba el registro para determinar qué proveedores de red están instalados en el sistema y el orden en el que deben recorrerse. Carga todas las dll de proveedor de red registradas y las utiliza para procesar las llamadas de WNet posteriores realizadas por la interfaz de usuario u otras aplicaciones.

Para obtener más información acerca de las funciones de WNet, consulte [redes de Windows](../wnet/windows-networking-wnet-.md).

 

 
