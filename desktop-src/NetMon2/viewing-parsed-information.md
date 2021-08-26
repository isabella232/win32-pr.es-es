---
description: El Monitor de red de fotogramas muestra los datos analizados en tres paneles.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Ver información analizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f01cfc0df45f2fb6ef0e1342d7fe54e5ed5701bad8ba1635dc13f4546b10e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962695"
---
# <a name="viewing-parsed-information"></a>Ver información analizada

El Monitor de red de fotogramas muestra los datos analizados en tres paneles. En el panel superior se muestra un resumen del marco que incluye el protocolo identificado. El panel central muestra las propiedades de datos con formato que se pueden organizar jerárquicamente como parte de la presentación del analizador. El panel inferior muestra los datos sin procesar resaltados que se seleccionan en el panel central.

Puede especificar cómo se muestra la información en el visor al desarrollar su propio analizador. En la ilustración siguiente se muestra cómo se puede mostrar la información en el Monitor de red de fotogramas.

![visor de fotogramas del monitor de red](images/parseui.png)

> [!Note]  
> Los analizadores no muestran fotogramas. Los analizadores reconocen los campos de la información proporcionada y, a continuación, notifican a Monitor de red que muestren el marco. El filtrado es una operación de nivel superior que permite que las consultas de filtro abarquen los analizadores.

 

En el analizador, use solo funciones que se puedan ejecutar en aplicaciones De Microsoft Win32. Antes de adjuntar propiedades a los datos sin procesar, un analizador debe registrar primero todas las propiedades posibles con el kernel Monitor de red datos. El analizador envía un mensaje al kernel para crear una base de datos de propiedades y, a continuación, rellena la base de datos de propiedades con todas las propiedades posibles para su protocolo. Cada propiedad de la base de datos de propiedades contiene información como una descripción textual, un tipo de datos y un calificador que se usan para dar formato a los datos sin procesar y una rutina de formato que se usa para mostrar los datos.

 

 



