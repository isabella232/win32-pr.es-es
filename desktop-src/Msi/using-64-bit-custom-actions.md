---
description: En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 o 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso de acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d94e5d6118c0f2f5dcf5a297718e135cce25a69bea0f48a2d4ea5df4cc0463
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809115"
---
# <a name="using-64-bit-custom-actions"></a>Uso de acciones personalizadas de 64 bits

En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 o 64 bits. Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de acción personalizada en la columna Type de la [tabla CustomAction](customaction-table.md). Las acciones [](executable-files.md) personalizadas basadas en archivos ejecutables o bibliotecas de [vínculos dinámicos](dynamic-link-libraries.md) que se cumplen con los sistemas operativos de 64 bits no requieren incluir este bit adicional en la columna Tipo de la tabla CustomAction.

Para obtener más información, vea Acciones personalizadas de [64 bits.](64-bit-custom-actions.md)

 

 



