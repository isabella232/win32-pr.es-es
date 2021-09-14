---
description: La capa de datos a menudo contiene principalmente información estática&\# 8212; información persistente en medios duraderos.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimización de llamadas entre la lógica de negocios y los datos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965148"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Optimización de interacciones entre el nivel de lógica de negocios de COM+ y el nivel de datos

La capa de datos a menudo contiene principalmente información estática, información que se conserva en medios duraderos. Dado que este nivel abarca información que es principalmente estática, requiere un análisis exhaustivo de posibles cuellos de botella. Además de la posibilidad obvia de cuellos de botella de conexión, las zonas activas pueden deberse a registros a los que se accede con frecuencia, a métodos de acceso a datos ineficaces y a la necesidad de coordinar el acceso a los sistemas heredados.

## <a name="connecting-to-the-data-tier"></a>Conexión a la capa de datos

Dos consideraciones desempeñan un papel importante en el diseño de una capa de datos para una aplicación COM+: la agrupación de conexiones y la activación [Just-In-Time (JIT)](com--just-in-time-activation.md)de COM+ y el uso de DSN. Los componentes que realicen conexiones a la capa de datos deben usar el conjunto de agrupación de objetos [COM+](com--object-pooling.md) en el componente.

Al crear DSN, use las cadenas de constructor de objetos especificadas en el componente en lugar de crear un DSN de archivo. Los DSN de archivo son más lentos que una conexión mediante una cadena de constructor de objetos. Las cadenas de constructor de objetos se pueden especificar en la hoja de propiedades del componente. Para obtener más información, [vea Cadenas de constructor de objetos COM+.](com--object-constructor-strings.md)

Si usa componentes para acceder a una base de SQL Server, use la agrupación de objetos COM+ en lugar de SQL agrupación de conexiones.

Si el componente usa ADO para capturar varios conjuntos de registros, establezca varias conexiones para el componente. Cuando ADO recupera varios conjuntos de registros, crea varias conexiones en segundo plano si no las crea. Si los crea, puede agruparlos y tener más control sobre el número de conexiones usadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Optimización de interacciones entre el nivel de lógica de negocios de COM+ y el nivel de presentación](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



