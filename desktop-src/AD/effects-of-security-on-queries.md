---
title: Efectos de la seguridad en la búsqueda
description: La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efectos de la seguridad en la búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773236"
---
# <a name="effects-of-security-on-searching"></a>Efectos de la seguridad en la búsqueda

La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.

ADSI no puede devolver ninguna \_ propiedad de este tipo, \_ ni \_ \_ siquiera cuando el objeto existe si no tiene acceso para leer atributos en el objeto.

Por ejemplo, un llamador puede enumerar los objetos secundarios de un contenedor porque el autor de la llamada tiene \_ derechos de lista de contenido en el contenedor. Pero es posible que el mismo llamador no pueda tener acceso a los objetos enumerados si el autor de la llamada no tiene acceso de lectura a los objetos secundarios. En este caso, es posible que una consulta para un objeto secundario NO devuelva \_ este tipo de \_ objeto aunque el autor de la llamada haya enumerado correctamente el objeto.

Si el autor de la llamada no tiene derechos suficientes, se pueden devolver los siguientes códigos de retorno:

E \_ ADS \_ \_ objeto de dominio no válido \_

\_no se \_ admite la propiedad de ADS \_ \_

\_ \_ \_ no \_ se encontró la propiedad de ADS

 

 




