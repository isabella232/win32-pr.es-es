---
description: Las aplicaciones Unicode siempre deben convertir cero en TCHAR al usar cadenas terminadas en NULL.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Usar cadenas terminadas en null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279493"
---
# <a name="using-null-terminated-strings"></a>Usar cadenas terminadas en null

Las aplicaciones Unicode siempre deben convertir cero en TCHAR al usar cadenas terminadas en NULL. El código 0x0000 es el terminador de cadena Unicode para una cadena terminada en NULL. Un solo byte nulo no es suficiente para este código, ya que muchos caracteres Unicode contienen bytes NULL como byte alto o bajo. Un ejemplo es la letra A, para la que el código de carácter es 0x0041.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



