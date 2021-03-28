---
description: La región de actualización identifica la parte de una ventana que no está actualizada o no es válida y en la que es necesario volver a dibujar.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: La región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997913"
---
# <a name="the-update-region"></a>La región de actualización

La *región de actualización* identifica la parte de una ventana que no está actualizada o no es válida y en la que es necesario volver a dibujar. El sistema utiliza la región de actualización para generar mensajes de [**WM \_ Paint**](wm-paint.md) para las aplicaciones y para minimizar el tiempo que las aplicaciones dedican a poner el contenido de sus ventanas al día. El sistema solo agrega la parte no válida de la ventana a la región de actualización, por lo que solo se debe dibujar esa parte.

Cuando el sistema determina que es necesario actualizar una ventana, establece las dimensiones de la región de actualización en la parte no válida de la ventana. La configuración de la región de actualización no hace que la aplicación se dibuje inmediatamente. En su lugar, la aplicación continúa recuperando mensajes de la cola de mensajes de la aplicación hasta que no quedan mensajes. Después, el sistema comprueba la región de actualización y, si la región no está vacía (no NULL), envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) al procedimiento de ventana.

Una aplicación puede usar la región de actualización para generar sus mensajes de [**WM \_ Paint**](wm-paint.md) . Por ejemplo, una aplicación que carga datos de archivos abiertos normalmente establece la región de actualización durante la carga, de modo que los nuevos datos se dibujen durante el procesamiento del siguiente mensaje de **\_ dibujo de WM** . En general, una aplicación no debe dibujar en el momento en que los datos cambian, pero enrutar todas las operaciones de dibujo a través del mensaje de **\_ Paint de WM** .

 

 



