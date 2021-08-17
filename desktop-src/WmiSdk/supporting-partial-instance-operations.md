---
description: No es necesario que un proveedor admita ninguna operación de instancia parcial. Sin embargo, un proveedor debe admitir toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver WBEM \_ E \_ UNSUPPORTED \_ PARAMETER.
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Compatibilidad con Partial-Instance operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922855"
---
# <a name="supporting-partial-instance-operations"></a>Compatibilidad con Partial-Instance operaciones

No es necesario que un proveedor admita ninguna operación de instancia parcial. Sin embargo, un proveedor debe admitir toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER**.

Al crear un proveedor que admita operaciones de instancia parcial, debe observar las siguientes reglas:

-   Reutilice el mismo objeto de contexto que WMI envía al proveedor. WMI usa el valor con nombre \_ \_ "GET EXT CLIENT REQUEST" para evitar interbloqueos y quita este cliente antes de reenviar el objeto de contexto \_ \_ a un \_ proveedor.
-   En el caso de las llamadas reentrante a WMI que no requieren una operación de instancia parcial, asegúrese de devolver el mismo objeto de contexto sin modificaciones. WMI recibe el objeto de contexto sin el conjunto de valores con nombre \_ \_ "GET \_ EXT CLIENT REQUEST" y elimina todos los valores con nombre \_ asociados a las operaciones de instancia parcial del objeto de contexto antes de pasarlo a otros \_ proveedores. No cambiar el objeto de contexto impide que otros proveedores reciban operaciones de recuperación de instancias parciales destinadas a un objeto diferente no relacionado.
-   Para realizar una operación de instancia parcial reentrante mientras se lleva a cabo una solicitud, establezca el valor y la propiedad con nombre \_ \_ "GET \_ EXT \_ CLIENT \_ REQUEST" ausentes. Opcionalmente, puede modificar las propiedades del valor con nombre "GET EXT PROPERTIES" antes de devolver el objeto de contexto a WMI con la \_ \_ \_ \_ llamada reentrante.
-   No acceda al objeto de contexto después de devolverlo a WMI durante una llamada reentrante; otros proveedores pueden modificar las listas de propiedades u otros valores durante la reenlazancia. Puede examinar o modificar el objeto de contexto solo mientras dure la llamada [**a IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que implemente.

 

 



