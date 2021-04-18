---
description: No es necesario que un proveedor admita las operaciones de instancia parcial. Sin embargo, un proveedor debe ser compatible con toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver un \_ \_ parámetro no compatible de WBEM E \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Compatibilidad con operaciones de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706078"
---
# <a name="supporting-partial-instance-operations"></a>Compatibilidad con operaciones de Partial-Instance

No es necesario que un proveedor admita las operaciones de instancia parcial. Sin embargo, un proveedor debe ser compatible con toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver **un \_ \_ \_ parámetro no compatible de WBEM E**.

Al crear un proveedor que admita operaciones de instancia parcial, debe observar las siguientes reglas:

-   Reutilice el mismo objeto de contexto que WMI envía al proveedor. WMI usa el \_ \_ \_ \_ \_ valor con nombre "obtener solicitud de cliente ext" para evitar interbloqueos y quita este cliente antes de reenviar el objeto de contexto a un proveedor.
-   En el caso de las llamadas reentrantes a WMI que no requieran una operación de instancia parcial, asegúrese de volver a pasar el mismo objeto de contexto sin ninguna modificación. WMI recibe el objeto de contexto sin el \_ \_ \_ \_ valor con nombre "Get ext Client \_ Request" establecido y elimina todos los valores con nombre asociados a las operaciones de instancia parcial del objeto de contexto antes de pasarlos a otros proveedores. No cambiar el objeto de contexto impide que otros proveedores reciban operaciones de recuperación de instancia parcial destinadas a un objeto diferente no relacionado.
-   Para realizar una operación de instancia parcial reentrante mientras se lleva a cabo una solicitud, establezca el \_ \_ \_ \_ valor y la propiedad "obtener solicitud de cliente ext \_ " que faltan. Opcionalmente, puede modificar las propiedades en el \_ \_ \_ \_ valor con nombre "obtener propiedades ext" antes de volver a enviar el objeto de contexto a WMI con la llamada reentrante.
-   No tener acceso al objeto de contexto después de devolverlo a WMI durante una llamada reentrante; otros proveedores pueden modificar las listas de propiedades u otros valores durante la reentrada. Puede examinar o modificar el objeto de contexto solo mientras dure la llamada a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que implemente.

 

 



