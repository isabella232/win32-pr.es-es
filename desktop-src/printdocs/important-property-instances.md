---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instancias de propiedad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721381"
---
# <a name="important-property-instances"></a>Instancias de propiedad importantes

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para que un cliente de PrintCapabilities pueda construir un PrintTicket razonable, el documento de PrintCapabilities debe proporcionar ciertas propiedades de instancias de características, así como instancias de opciones dentro de la característica. Un módulo de interfaz de usuario (IU) genérico requiere tal información para construir una interfaz de usuario. Esto a su vez requiere que las palabras clave de esquema de impresión definan algunas instancias de propiedad que aparecen como elementos secundarios de los elementos de opción y de característica.

Los elementos de característica pueden contener la siguiente propiedad.



| Propiedad                  | Valores                                 | Propósito                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Especifica el número de opciones que se pueden seleccionar para esta característica en un momento dado, ya sea una (PickOne) o más de una (PickMany). El cliente puede utilizar esta información para construir un PrintTicket. Esta información afecta al comportamiento de la interfaz de usuario, así como a la validación de PrintTicket por parte del proveedor.<br/> |



 

Los elementos de opción pueden contener la siguiente propiedad.



| Propiedad                   | Valores                           | Propósito                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | True<br/> False<br/> | La selección de la propiedad IdentityOption se interpreta para indicar "deshabilitar esta característica". Una característica que contiene una propiedad SelectionType cuyo valor es PickMany también debe contener una opción que tenga una propiedad IdentityOption. El código de la interfaz de usuario (o el cliente que crea un PrintTicket) debe anular la selección de cualquier otra opción si la propiedad IdentityOption está seleccionada.<br/> |



 

Los elementos Feature, Option y ParameterDef pueden contener la siguiente propiedad.



| Propiedad              | Valores                          | Propósito                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Mostrar<br/> Ocultar<br/> | Especifica si el elemento primario se debe mostrar en la interfaz de usuario. Mostrar indica que el elemento debe mostrarse en la interfaz de usuario. Hide indica que el elemento no se debe mostrar en la interfaz de usuario. Si esta propiedad no está definida para un elemento, se muestra la interpretación predeterminada, lo que significa que se muestra el elemento.<br/> |



 

Los elementos Feature, Option y ParameterDef pueden contener la siguiente propiedad.



| Propiedad                | Value             | Propósito                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | String<br/> | Especifica la cadena de presentación para el elemento primario, invalidando el nombre para mostrar predeterminado. Los proveedores de PrintCapabilities pueden utilizar para presentar un nombre para mostrar localizado y descriptivo para el usuario. El valor de nombre para mostrar predeterminado es el atributo de nombre del elemento primario. <br/> En el caso de los elementos Option, si no se proporciona el atributo name, la propiedad DisplayName debe estar presente.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




