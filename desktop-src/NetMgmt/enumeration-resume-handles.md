---
title: Identificadores de reanudación de enumeración
description: Los identificadores de reanudación de enumeración son identificadores de la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del autor de la llamada para la función.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069416"
---
# <a name="enumeration-resume-handles"></a>Identificadores de reanudación de enumeración

Los identificadores de reanudación de enumeración son identificadores de la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del autor de la llamada para la función.

Si se **pasa un valor NULL** para el puntero al identificador de reanudación, no se almacena ningún identificador y no se puede continuar la búsqueda de enumeración. Esto resulta útil en casos en los que la aplicación no desea enumerar todos los elementos.

Si se devuelve un error de una llamada de enumeración, el identificador de reanudación debe tratarse como no válido y no usarse para las llamadas de enumeración posteriores. Cuando esto ocurre, debe reiniciar la enumeración desde el principio.

 

 




