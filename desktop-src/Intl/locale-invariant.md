---
description: LOCALE \_ INVARIANT
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c3a4bddaaa51ca72be9d48f273ac0cbd1727e18e5c821e8ce86acaf0f90ec4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106585"
---
# <a name="locale_invariant"></a>LOCALE \_ INVARIANT

**Windows XP:** Configuración regional usada para las funciones de nivel de sistema operativo que requieren resultados coherentes e independientes de la configuración regional. Por ejemplo, la configuración regional invariable se usa cuando una aplicación compara cadenas de caracteres mediante la [**función CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y espera un resultado coherente independientemente de la configuración regional del usuario. La configuración de la configuración regional invariable es similar a la del inglés (Estados Unidos), pero no se debe usar para mostrar datos con formato. Normalmente, una aplicación no usa LOCALE INVARIANT porque espera que los resultados de una acción dependan de las reglas que rigen cada \_ configuración regional individual. El valor de LOCALE \_ INVARIANT ES 0x007f.

 

 
