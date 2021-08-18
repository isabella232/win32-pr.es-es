---
description: Los escapes de impresora proporcionados por los dispositivos de 16 Windows permitir el acceso a características especiales del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711565"
---
# <a name="printer-escapes"></a>Escapes de impresora

Los escapes de impresora proporcionados por los dispositivos de 16 Windows permitir el acceso a características especiales del dispositivo. La mayoría de estos escapes están obsoletos, pero se proporcionan algunos para simplificar la porte de aplicaciones basadas en Windows bits. GDI admite un conjunto completo de funciones de ruta de acceso que las aplicaciones pueden usar en lugar de los escapes para dibujar rutas de acceso en cualquier dispositivo. Para obtener una lista de funciones que reemplazan a algunos de los escapes, consulte la [**función Escape.**](/windows/desktop/api/Wingdi/nf-wingdi-escape)

De los 64 escapes de impresora originales, solo se pueden usar **QUERYESCSUPPORT** y **PASSTHROUGH.**

También hay una función de escape extendida denominada [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) Esta función permite que las aplicaciones accedan a funcionalidades de un dispositivo determinado que no están disponibles directamente a través de GDI.

 

 



