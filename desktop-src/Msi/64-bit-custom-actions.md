---
description: En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 bits o de 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813371"
---
# <a name="64-bit-custom-actions"></a>Acciones personalizadas de 64 bits

En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 bits o de 64 bits.

Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico Actions personalizado en la columna Type de la [tabla CustomAction](customaction-table.md).



| Constante                             | Hexadecimal | Decimal | Significado                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Se trata de una acción personalizada de 64 bits escrita en [scripts](scripts.md). |



 

Las acciones personalizadas basadas en [archivos ejecutables](executable-files.md) o [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) que se han cumplido para los sistemas operativos de 64 bits no requieren incluir este bit adicional en la columna de tipo de la tabla CustomAction.

 

 



