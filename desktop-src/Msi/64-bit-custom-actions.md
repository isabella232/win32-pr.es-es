---
description: En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se han compilado para sistemas de 32 o 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159287"
---
# <a name="64-bit-custom-actions"></a>Acciones personalizadas de 64 bits

En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se han compilado para sistemas de 32 o 64 bits.

Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de acciones personalizadas en la columna Type de la [tabla CustomAction](customaction-table.md).



| Constante                             | Hexadecimal | Decimal | Significado                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Se trata de una acción personalizada de 64 bits escrita en [Scripts](scripts.md). |



 

Las acciones [](executable-files.md) personalizadas basadas en archivos ejecutables o bibliotecas de [vínculos dinámicos](dynamic-link-libraries.md) que se han cumplido para sistemas operativos de 64 bits no requieren incluir este bit adicional en la columna Tipo de la tabla CustomAction.

 

 



