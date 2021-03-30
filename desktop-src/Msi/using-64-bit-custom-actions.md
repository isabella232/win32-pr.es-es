---
description: En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se compilan para sistemas de 32 bits o de 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso de acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002361"
---
# <a name="using-64-bit-custom-actions"></a>Uso de acciones personalizadas de 64 bits

En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se compilan para sistemas de 32 bits o de 64 bits. Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de la acción personalizada en la columna tipo de la [tabla CustomAction](customaction-table.md). Las acciones personalizadas basadas en [archivos ejecutables](executable-files.md) o [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) que se cumplen para los sistemas operativos de 64 bits no requieren que se incluya este bit adicional en la columna tipo de la tabla CustomAction.

Para obtener más información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).

 

 



