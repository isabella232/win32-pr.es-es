---
description: Todos los objetos protegibles organizan sus derechos de acceso mediante el formato de máscara de acceso que se muestra en la ilustración siguiente.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato de máscara de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86187f5ef69eb115bc880d2bc4df07e8b1a1f791976da2a8d24b6a0f9d7293c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914540"
---
# <a name="access-mask-format"></a>Formato de máscara de acceso

Todos los objetos protegibles organizan sus derechos de acceso mediante el formato [*de*](/windows/desktop/SecGloss/a-gly) máscara de acceso que se muestra en la ilustración siguiente.

![formato de máscara de acceso](images/accctrl4.png)

En este formato, los 16 bits de orden inferior son para los derechos de acceso específicos del objeto, los 8 bits siguientes son [](generic-access-rights.md) para los derechos de acceso estándar [,](standard-access-rights.md)que se aplican a la mayoría de los tipos de objetos, y los 4 bits de orden superior se usan para especificar derechos de acceso genéricos que cada tipo de objeto puede asignar a un conjunto de derechos estándar y específicos del objeto. El bit ACCESS SYSTEM SECURITY corresponde a la derecha para acceder a la \_ \_ [SACL del objeto](sacl-access-right.md).

 

 
