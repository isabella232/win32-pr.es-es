---
title: Identificadores de reanudación de enumeración
description: Los identificadores de reanudación de enumeración son identificadores para la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del llamador de la función.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994257"
---
# <a name="enumeration-resume-handles"></a>Identificadores de reanudación de enumeración

Los identificadores de reanudación de enumeración son identificadores para la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del llamador de la función.

Si se pasa un **valor null** para el puntero al controlador de reanudación, no se almacena ningún identificador y no se puede continuar la búsqueda de enumeración. Esto resulta útil en los casos en los que la aplicación no desea enumerar todos los elementos.

Si se devuelve un error de una llamada de enumeración, el controlador de reanudación se debe tratar como no válido y no se puede usar para las llamadas de enumeración posteriores. Cuando esto sucede, debe reiniciar la enumeración desde el principio.

 

 




