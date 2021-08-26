---
description: La aplicación puede solicitar uno de estos dos modos de funcionamiento al abrir un dispositivo de teléfono.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modos de funcionamiento y privilegios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012475"
---
# <a name="operating-modes-and-privileges"></a>Modos de funcionamiento y privilegios

La aplicación puede solicitar uno de estos dos modos de funcionamiento al abrir un dispositivo de teléfono. Estos modos reflejan los privilegios que solicita la aplicación para el dispositivo:

-   Abrir un teléfono para los privilegios de supervisión permite a la aplicación determinar el estado del dispositivo telefónico. Los mensajes se envían a la aplicación cuando se detectan cambios de estado en el dispositivo telefónico.
-   Una aplicación que abre un dispositivo de teléfono con privilegios de propietario puede usar operaciones que modifiquen el estado del dispositivo telefónico. Los privilegios de propietario también incluyen automáticamente privilegios de supervisión completos. En cualquier momento, un dispositivo de teléfono determinado solo se puede abrir una vez para los privilegios de propietario, pero varias veces para los privilegios de supervisión. Todas **las operaciones phoneSet** requieren privilegios de propietario, mientras que todas las **operaciones phoneGet** solo requieren privilegios de supervisión.

 

 



