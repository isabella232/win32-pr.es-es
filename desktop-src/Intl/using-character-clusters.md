---
description: Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso de clústeres de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819006"
---
# <a name="using-character-clusters"></a>Uso de clústeres de caracteres

Los clústeres de caracteres son secuencias de glifo que no se pueden dividir entre líneas. Algunos lenguajes, por ejemplo tailandés e hindú, restringen la colocación del símbolo de intercalación a puntos entre los clústeres. Esta restricción se aplica al movimiento de intercalación iniciado con las acciones del teclado o del mouse (prueba de posicionamiento).

Uniscribe proporciona información del clúster en los atributos visuales contenidos en una estructura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) y los atributos lógicos contenidos en una estructura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Una vez que la aplicación llama a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), la información del clúster se representa mediante secuencias del mismo valor en la matriz de **\_ LOGATTR de script** y el miembro **fClusterStart** de la matriz de **script \_ VISATTR** .

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) también recupera el miembro **fCharStop** de la estructura [**\_ LOGATTR del script**](/windows/win32/api/usp10/ns-usp10-script_logattr) para identificar las posiciones del clúster.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



