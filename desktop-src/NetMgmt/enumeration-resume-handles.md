---
title: Identificadores de reanudación de enumeración
description: Los identificadores de reanudación de enumeración son identificadores de la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del autor de la llamada para la función.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10976661723af59af945b9dec1080196e682b308fa1a597edfc4cee6047aa783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912195"
---
# <a name="enumeration-resume-handles"></a>Identificadores de reanudación de enumeración

Los identificadores de reanudación de enumeración son identificadores de la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del autor de la llamada para la función.

Si se **pasa un valor NULL** para el puntero al identificador de reanudación, no se almacena ningún identificador y no se puede continuar con la búsqueda de enumeración. Esto es útil en los casos en los que la aplicación no quiere enumerar todos los elementos.

Si se devuelve un error de una llamada de enumeración, el identificador de reanudación debe tratarse como no válido y no usarse para las llamadas de enumeración posteriores. Cuando esto sucede, debe reiniciar la enumeración desde el principio.

 

 




