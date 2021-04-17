---
description: configuración regional \_ INvariable
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652415"
---
# <a name="locale_invariant"></a>configuración regional \_ INvariable

**Windows XP:** Configuración regional que se usa para las funciones de nivel de sistema operativo que requieren resultados coherentes y independientes de la configuración regional. Por ejemplo, la configuración regional invariable se usa cuando una aplicación compara cadenas de caracteres mediante la función [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y espera un resultado coherente independientemente de la configuración regional del usuario. La configuración regional de todos los idiomas es similar a la de inglés (Estados Unidos), pero no debe usarse para Mostrar datos con formato. Normalmente, una aplicación no usa la configuración regional \_ invariable, ya que espera que los resultados de una acción dependan de las reglas que rigen cada configuración regional individual. El valor de configuración regional \_ INVARIABLE es 0x007f.

 

 
