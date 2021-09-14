---
description: Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso de clústeres de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254895"
---
# <a name="using-character-clusters"></a>Uso de clústeres de caracteres

Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas. Algunos idiomas, por ejemplo, tailandés e indic, restringen la colocación del signo de inserción a puntos entre clústeres. Esta restricción se aplica al movimiento del cursor de cursor iniciado con acciones del teclado o del mouse (pruebas de pulsación).

Uniscribe proporciona información de clúster en los atributos visuales contenidos en una estructura [**\_ SCRIPT RGPDTTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) y en los atributos lógicos contenidos en una [**estructura \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) de SCRIPT. Después de que la aplicación llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), la información del clúster se representa mediante secuencias del mismo valor en la matriz **\_ LOGATTR** de SCRIPT y por el miembro **fClusterStart** en la matriz **SCRIPT SCRIPTS \_ SCRIPTSTTR.**

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) también recupera el miembro **fCharStop** de la estructura [**\_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) de SCRIPT para identificar las posiciones del clúster.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



