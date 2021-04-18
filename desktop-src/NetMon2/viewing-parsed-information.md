---
description: En el visor de fotogramas Monitor de red se muestran los datos analizados en tres paneles.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Ver información analizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562758"
---
# <a name="viewing-parsed-information"></a>Ver información analizada

En el visor de fotogramas Monitor de red se muestran los datos analizados en tres paneles. En el panel superior se muestra un resumen del marco que incluye el protocolo identificado. En el panel central se muestran las propiedades de los datos con formato que se pueden organizar jerárquicamente como parte de la presentación del analizador. En el panel inferior se muestran los datos sin procesar resaltados que se seleccionan en el panel central.

Puede especificar cómo se muestra la información en el visor al desarrollar su propio analizador. En la ilustración siguiente se muestra cómo se puede mostrar información en el visor de tramas de Monitor de red.

![visor de tramas del monitor de red](images/parseui.png)

> [!Note]  
> Los analizadores no muestran fotogramas. Los analizadores reconocen los campos en la información proporcionada y, a continuación, notifican a Monitor de red para mostrar el marco. El filtrado es una operación de nivel superior que permite que las consultas de filtro abarquen los analizadores.

 

En el analizador, use solo funciones que se puedan ejecutar en aplicaciones de Microsoft Win32. Antes de adjuntar propiedades a los datos sin procesar, un analizador debe registrar primero todas las propiedades posibles con el kernel Monitor de red. El analizador envía un mensaje al kernel para crear una base de datos de propiedades y, a continuación, rellena la base de datos de propiedades con cada propiedad posible para su Protocolo. Cada propiedad de la base de datos de propiedades contiene información como, por ejemplo, una descripción textual, un tipo de datos y un calificador que se usan para dar formato a los datos sin procesar y una rutina de formato que se usa para mostrar los datos.

 

 



