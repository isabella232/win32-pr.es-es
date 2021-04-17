---
title: Qué puede saber y cuándo puede saberlo
description: Las aplicaciones que son sensibles a los Estados inducidos por latencia deben reconocer los Estados de los problemas y tomar las medidas adecuadas.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656213"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>¿Qué puede saber y cuándo puede saberlo?

Las aplicaciones que son sensibles a los Estados inducidos por latencia deben reconocer los Estados de los problemas y tomar las medidas adecuadas. Hay dos Estados de problema: sesgo de versión y actualización parcial. El sesgo de versiones no se detecta examinando el servicio de directorio (Recuerde el axioma de la informática distribuida que se indica en [qué Active Directory Domain Services usar este modelo de replicación](why-active-directory-domain-services-uses-this-replication-model.md)). La actualización parcial se puede detectar agregando metadatos a los objetos que componen el conjunto relacionado. En secciones posteriores de este documento aparecen sugerencias para estos metadatos. Existen estrategias de prevención que las aplicaciones pueden tomar para reducir la posibilidad de que se produzcan sesgos de versiones y actualizaciones parciales. Estas estrategias también se tratan en secciones posteriores de este documento.

 

 




