---
title: Efectos de la seguridad en la búsqueda
description: La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efectos de la seguridad en la búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191625"
---
# <a name="effects-of-security-on-searching"></a>Efectos de la seguridad en la búsqueda

La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.

ADSI puede devolver errores NO SUCH PROPERTY o NO SUCH OBJECT incluso cuando el objeto existe si no tiene acceso para leer \_ \_ atributos en el \_ \_ objeto.

Por ejemplo, un autor de la llamada puede enumerar los objetos secundarios de un contenedor porque el autor de la llamada tiene derechos LIST \_ CONTENTS en el contenedor. Pero es posible que el mismo autor de la llamada no pueda acceder a los objetos enumerados si el autor de la llamada no tiene acceso de lectura a los objetos secundarios. En este caso, una consulta para un objeto secundario puede devolver NO SUCH OBJECT aunque el autor de la llamada \_ \_ enumerase correctamente el objeto.

Si el autor de la llamada no tiene derechos suficientes, se pueden devolver los siguientes códigos de retorno:

E \_ ADS \_ INVALID \_ DOMAIN \_ OBJECT

NO \_ SE ADMITE LA PROPIEDAD E \_ \_ \_ ADS

E \_ ADS \_ PROPERTY \_ NOT \_ FOUND

 

 




