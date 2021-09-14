---
description: LOCALE \_ INVARIANT
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274468"
---
# <a name="locale_invariant"></a>LOCALE \_ INVARIANT

**Windows XP:** Configuración regional usada para las funciones de nivel de sistema operativo que requieren resultados coherentes e independientes de la configuración regional. Por ejemplo, la configuración regional invariable se usa cuando una aplicación compara cadenas de caracteres mediante la [**función CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y espera un resultado coherente independientemente de la configuración regional del usuario. La configuración de la configuración regional invariable es similar a la del inglés (Estados Unidos), pero no se debe usar para mostrar datos con formato. Normalmente, una aplicación no usa LOCALE INVARIANT porque espera que los resultados de una acción dependan de las reglas que rigen cada \_ configuración regional individual. El valor de LOCALE \_ INVARIANT IS 0x007f.

 

 
