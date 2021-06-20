---
description: Para que un cliente construya un PrintTicket, el documento PrintCapabilities debe proporcionar propiedades de instancias de características e instancias de opción en la característica.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instancias de propiedad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409128"
---
# <a name="important-property-instances"></a>Instancias de propiedad importantes

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para que un cliente PrintCapabilities pueda construir un PrintTicket razonable, el documento PrintCapabilities debe proporcionar determinadas propiedades de instancias de características, así como instancias de option dentro de la característica. Un módulo de interfaz de usuario (UI) genérico requiere dicha información para construir una interfaz de usuario. Esto, a su vez, requiere que las palabras clave de esquema de impresión definan algunas instancias de propiedad que aparecen como elementos secundarios de los elementos Feature y Option.

Los elementos feature pueden contener la propiedad siguiente.



| Propiedad                  | Valores                                 | Propósito                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Especifica el número de opciones que se pueden seleccionar para esta característica en un momento dado, uno (PickOne) o más de uno (PickMany). El cliente puede usar esta información para construir un PrintTicket. Esta información afecta al comportamiento de la interfaz de usuario, así como a la validación de PrintTicket por parte del proveedor.<br/> |



 

Los elementos Option pueden contener la propiedad siguiente.



| Propiedad                   | Valores                           | Propósito                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | True<br/> False<br/> | La selección de la propiedad IdentityOption se interpreta como "deshabilitar esta característica". Una característica que contiene una propiedad SelectionType cuyo valor es PickMany también debe contener una opción que tenga una propiedad IdentityOption. El código de la interfaz de usuario (o el cliente que construye un PrintTicket) debe anular la selección de cualquier otra opción si está seleccionada la propiedad IdentityOption.<br/> |



 

Los elementos Feature, Option y ParameterDef pueden contener la propiedad siguiente.



| Propiedad              | Valores                          | Propósito                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Mostrar<br/> Ocultar<br/> | Especifica si el elemento primario debe mostrarse en la interfaz de usuario. Mostrar indica que el elemento debe mostrarse en la interfaz de usuario. Ocultar indica que el elemento no debe mostrarse en la interfaz de usuario. Si esta propiedad no está definida para un elemento, la interpretación predeterminada es Show, lo que significa que se muestra el elemento .<br/> |



 

Los elementos Feature, Option y ParameterDef pueden contener la propiedad siguiente.



| Propiedad                | Value             | Propósito                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | String<br/> | Especifica la cadena para mostrar del elemento primario, reemplazando el nombre para mostrar predeterminado. Los proveedores de PrintCapabilities pueden usar para presentar un nombre para mostrar localizado y descriptivo. El valor predeterminado del nombre para mostrar es el atributo name del elemento primario. <br/> En el caso de los elementos Option, si no se proporciona el atributo name, debe estar presente la propiedad DisplayName.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




