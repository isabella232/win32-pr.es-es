---
title: Trasladar funciones de suavizado de contorno
description: Trasladar funciones de suavizado de contorno
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Migración de la contabilidad de IRIS y suavizado de contorno
- portabilidad de IRIS GL, antialiasing
- trasladar a OpenGL desde IRIS GL, suavizado de contorno
- Exportación de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419124"
---
# <a name="porting-antialiasing-functions"></a>Trasladar funciones de suavizado de contorno

En OpenGL, el modo de subpíxeles está siempre activado, por lo tanto, el **subpíxel** de la función de contabilidad de iris no es necesario y no tiene ningún equivalente de OpenGL. En los temas siguientes se describen los aspectos del código de suavizado de contorno de la contabilidad de IRIS.

-   [Trasladar código de fusión](porting-blending-code.md)
-   [Portabilidad de las funciones de prueba de afunction](porting-afunction-test-functions.md)
-   [Usar funciones de suavizado de contorno](using-antialiasing-functions.md)

 

 




