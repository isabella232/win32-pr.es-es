---
description: Los escapes de impresora proporcionados por Windows de 16 bits permitían el acceso a las características especiales del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277437"
---
# <a name="printer-escapes"></a>Escapes de impresora

Los escapes de impresora proporcionados por Windows de 16 bits permitían el acceso a las características especiales del dispositivo. La mayoría de estos escapes están obsoletos, pero se proporcionan algunos para simplificar la migración de aplicaciones basadas en Windows de 16 bits. GDI admite un conjunto completo de funciones de ruta de acceso que las aplicaciones pueden usar en lugar de los escapes para dibujar trazados en cualquier dispositivo. Para obtener una lista de las funciones que reemplazan algunos de los escapes, vea la función [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

De los escapes de impresora originales 64, solo se pueden usar **QUERYESCSUPPORT** y **PASSTHROUGH** .

También hay una función de escape extendida denominada [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Esta función permite a las aplicaciones tener acceso a las capacidades de un dispositivo determinado que no están directamente disponibles a través de GDI.

 

 



