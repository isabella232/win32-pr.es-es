---
description: Puede modelar un proveedor de clases como un proveedor de inserción o de extracción, que especifica cómo un proveedor espera interactuar con WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinar el estado de inserción o de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715829"
---
# <a name="determining-push-or-pull-status"></a>Determinar el estado de inserción o de extracción

Puede modelar un proveedor de clases como un proveedor de inserción o de extracción, que especifica cómo un proveedor espera interactuar con WMI. Los proveedores de extracción reciben una solicitud de WMI y satisfacen la solicitud mediante la generación dinámica de los datos o la recuperación de una caché local. Los proveedores de extracción también deben implementar un gran número de interfaces.

Un proveedor de extracción genera dinámicamente definiciones de clase. Normalmente, los datos administrados por un proveedor de extracción cambian con frecuencia, lo que requiere que el proveedor genere la clase dinámicamente o recupere la clase de una caché local siempre que una aplicación emita una solicitud. Un proveedor de extracción debe implementar sus propios mecanismos de recuperación de datos, caché y notificación de eventos. Dado que la mayoría de los proveedores son proveedores de extracción, la documentación de este archivo supone que está creando un proveedor de extracción, a menos que se indique explícitamente lo contrario.

Por el contrario, WMI usa datos en el repositorio WMI para controlar todas las solicitudes de aplicación para los proveedores de inserciones. Los proveedores de inserciones también usan menos métodos de interfaz y, por tanto, son más fáciles de implementar. Un proveedor de inserciones usa el repositorio WMI como área de almacenamiento para obtener información sobre el objeto administrado y actualiza esa información solo durante la inicialización. Por ejemplo, el proveedor de clases WDM incluido en la sección WMI del kit de desarrollo de software (SDK) de Microsoft Windows se modela como un proveedor de inserciones.

Mediante el uso del repositorio WMI como área de almacenamiento, un proveedor de inserción obtiene las siguientes ventajas a través de un proveedor de extracción:

-   No es necesario que el proveedor implemente una memoria caché local para almacenar los datos.
-   No es necesario que el proveedor admita la recuperación de datos. en su lugar, el proveedor puede basarse en WMI para proporcionar compatibilidad de recuperación.
-   Cuando una aplicación solicita datos proporcionados por el proveedor, WMI cumple esa solicitud.
-   El proveedor también puede basarse en WMI para admitir la notificación de eventos.

Sin embargo, dado que un proveedor de inserciones solo se actualiza durante la inicialización, es posible que los cambios en una clase no se reflejen en el repositorio WMI durante algún tiempo. Por lo tanto, el modelo de proveedor de inserciones funciona mejor con las clases que cambian poco o más son completamente estáticas.

 

 



