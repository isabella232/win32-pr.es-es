---
description: En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 o 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso de acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069600"
---
# <a name="using-64-bit-custom-actions"></a>Uso de acciones personalizadas de 64 bits

En sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 o 64 bits. Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de acción personalizada en la columna Type de la [tabla CustomAction](customaction-table.md). Las acciones [](executable-files.md) personalizadas basadas en archivos ejecutables o bibliotecas de [vínculos dinámicos](dynamic-link-libraries.md) que se cumplen con los sistemas operativos de 64 bits no requieren incluir este bit adicional en la columna Tipo de la tabla CustomAction.

Para obtener más información, vea Acciones personalizadas de [64 bits.](64-bit-custom-actions.md)

 

 



