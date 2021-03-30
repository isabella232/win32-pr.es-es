---
description: Las transformaciones incrustadas se almacenan en el archivo. msi del paquete. Esto garantiza a los usuarios que la transformación está siempre disponible cuando el paquete de instalación está disponible. Como alternativa, se pueden proporcionar transformaciones a los usuarios como archivos. MST independientes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformaciones incrustadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082780"
---
# <a name="embedded-transforms"></a>Transformaciones incrustadas

Las transformaciones incrustadas se almacenan en el archivo. msi del paquete. Esto garantiza a los usuarios que la transformación está siempre disponible cuando el paquete de instalación está disponible. Como alternativa, se pueden proporcionar transformaciones a los usuarios como archivos. MST independientes.

Para agregar una transformación incrustada a la lista transformaciones, agregue un signo de dos puntos (:) prefijo al nombre de archivo. Dado que el instalador siempre puede obtener la transformación del almacenamiento en el archivo. msi, las transformaciones incrustadas no se almacenan en caché en el equipo del usuario. Las transformaciones incrustadas se pueden usar en combinación con transformaciones [protegidas](secured-transforms.md) o [transformaciones no seguras](unsecured-transforms.md). Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).

 

 



