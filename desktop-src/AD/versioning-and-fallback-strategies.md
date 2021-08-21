---
title: Estrategias de control de versiones y reserva
description: Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva aún no se ha alcanzado, la aplicación debe tratar la situación correctamente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Estrategias de control de versiones y reserva de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55226efcd72cec4f6dbe65447a945733dac88a56b976661bcf24564c9b366ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024423"
---
# <a name="versioning-and-fallback-strategies"></a>Estrategias de control de versiones y reserva

Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva aún no se ha alcanzado, la aplicación debe tratar la situación correctamente. Para algunas aplicaciones, la respuesta correcta es "volver atrás" a una versión anterior de los objetos en cuestión. Active Directory Domain Services proporcionar una instalación de control de versiones: las aplicaciones que desean esta funcionalidad deben proporcionarla ellos mismos. Los enfoques para el control de versiones incluyen mantener los valores "últimos buenos conocidos" almacenados en caché localmente y almacenar varios conjuntos de objetos en el directorio, por ejemplo, en contenedores "antiguos", "actuales" y "nuevos". Muchos otros esquemas son posibles.

Las implementaciones deben tener cuidado para evitar consecuencias no deseadas. Solo se debe usar una versión anterior de los objetos cuando se detecta una actualización parcial o los nuevos objetos aún no son "efectivos". Volver atrás porque algo en la aplicación "no funciona" podría eludir la intención de un administrador. Por ejemplo, dos equipos que anteriormente podían comunicarse podrían encontrarse incapaces de hacerlo debido a un cambio en la directiva de seguridad del protocolo de Internet (IPsec). Si esto es intencionado por parte del administrador, los sistemas afectados no deben volver a la directiva que les permitió comunicarse, ya que se trataría de una infracción de seguridad.

 

 




