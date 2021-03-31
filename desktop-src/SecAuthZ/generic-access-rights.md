---
description: Los objetos protegibles utilizan un formato de máscara de acceso en el que los cuatro bits de orden superior especifican derechos de acceso genéricos.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Derechos de acceso genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816022"
---
# <a name="generic-access-rights"></a>Derechos de acceso genéricos

Los objetos protegibles utilizan un [formato de máscara de acceso](access-mask-format.md) en el que los cuatro bits de orden superior especifican derechos de acceso genéricos. Cada tipo de objeto protegible asigna estos bits a un conjunto de sus derechos de acceso estándar y específicos del objeto. Por ejemplo, un objeto de archivo de Windows asigna el \_ bit de lectura genérico al control de lectura \_ y sincroniza los derechos de acceso estándar, así como los \_ \_ \_ \_ \_ \_ derechos de acceso de archivo lectura de datos, archivo de escritura EA y lectura de archivos. Otros tipos de objetos asignan el \_ bit de lectura genérico a cualquier conjunto de derechos de acceso adecuado para ese tipo de objeto.

Puede usar derechos de acceso genéricos para especificar el tipo de acceso que necesita al abrir un identificador de un objeto. Normalmente es más sencillo que especificar todos los derechos estándar y específicos correspondientes.

En la tabla siguiente se muestran las constantes definidas para los derechos de acceso genéricos.



| Constante         | Significado genérico            |
|------------------|----------------------------|
| todos GENÉRICOs \_     | Todos los derechos de acceso posibles |
| \_ejecución genérica | Ejecutar acceso             |
| \_lectura genérica    | acceso de lectura                |
| \_escritura genérica   | Acceso de escritura               |



 

Las aplicaciones que definen objetos protegibles privados también pueden usar los derechos de acceso genéricos.

 

 



