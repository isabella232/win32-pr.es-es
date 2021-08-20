---
description: Puede modelar un proveedor de clases como un proveedor de inserción o extracción, que especifica cómo espera un proveedor interactuar con WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinar el estado de inserción o extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df69fcc88195f26611636fc5292521ec31dd070fce53a61ea80ffebe310a9503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924829"
---
# <a name="determining-push-or-pull-status"></a>Determinar el estado de inserción o extracción

Puede modelar un proveedor de clases como un proveedor de inserción o extracción, que especifica cómo espera un proveedor interactuar con WMI. Los proveedores de extracción reciben una solicitud de WMI y satisfacen la solicitud mediante la generación dinámica de los datos o la recuperación de una caché local. Los proveedores de extracción también deben implementar un gran número de interfaces.

Un proveedor de extracción genera definiciones de clase dinámicamente. Normalmente, los datos administrados por un proveedor de extracción cambian con frecuencia, lo que requiere que el proveedor genere la clase dinámicamente o recupere la clase de una caché local cada vez que una aplicación emite una solicitud. Un proveedor de extracción debe implementar sus propios mecanismos de recuperación de datos, caché y notificación de eventos. Dado que la mayoría de los proveedores son proveedores de extracción, en la documentación de este archivo se supone que está creando un proveedor de extracción a menos que se indique explícitamente lo contrario.

En cambio, WMI usa datos en el repositorio WMI para controlar todas las solicitudes de aplicación para los proveedores de inserción. Los proveedores de inserción también usan menos métodos de interfaz y, por tanto, son más fáciles de implementar. Un proveedor de inserción usa el repositorio WMI como un área de almacenamiento para obtener información sobre el objeto administrado y actualiza esa información solo durante la inicialización. Por ejemplo, el proveedor de clases WDM incluido en la sección WMI del Kit de desarrollo de software (SDK) de Microsoft Windows se modela como un proveedor de inserción.

Al usar el repositorio WMI como área de almacenamiento, un proveedor de inserción obtiene las siguientes ventajas sobre un proveedor de extracción:

-   El proveedor no necesita implementar una caché local para almacenar datos.
-   El proveedor no necesita admitir la recuperación de datos; en su lugar, el proveedor puede confiar en WMI para proporcionar compatibilidad con la recuperación.
-   Cuando una aplicación solicita los datos proporcionados por el proveedor, WMI la cumple.
-   El proveedor también puede confiar en WMI para admitir la notificación de eventos.

Sin embargo, dado que un proveedor de inserción solo se actualiza durante la inicialización, es posible que los cambios en una clase no se reflejen en el repositorio WMI durante algún tiempo. Por lo tanto, el modelo del proveedor de inserción funciona mejor con clases que cambian poco o que son completamente estáticas.

 

 



