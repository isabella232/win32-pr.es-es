---
description: Las transformaciones insertadas se almacenan dentro .msi archivo del paquete. Esto garantiza a los usuarios que la transformación siempre está disponible cuando el paquete de instalación está disponible. Como alternativa, las transformaciones se pueden proporcionar a los usuarios como archivos .mst independientes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformaciones insertadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d7afb2b28599cb9ee2f10c4bc1fb25fbb0939fe68da5e817972eb8fc94236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637467"
---
# <a name="embedded-transforms"></a>Transformaciones insertadas

Las transformaciones insertadas se almacenan dentro .msi archivo del paquete. Esto garantiza a los usuarios que la transformación siempre está disponible cuando el paquete de instalación está disponible. Como alternativa, las transformaciones se pueden proporcionar a los usuarios como archivos .mst independientes.

Para agregar una transformación incrustada a la lista de transformaciones, agregue dos puntos (:) prefijo del nombre de archivo. Dado que el instalador siempre puede obtener la transformación del almacenamiento en el archivo .msi, las transformaciones insertadas no se almacenan en caché en el equipo del usuario. Las transformaciones insertadas se pueden usar en combinación con [transformaciones protegidas](secured-transforms.md) o [transformaciones no seguras.](unsecured-transforms.md) Para obtener más información, [vea Aplicar transformaciones.](applying-transforms.md)

 

 



