---
description: Las aplicaciones Unicode siempre deben convertir cero a TCHAR cuando se usan cadenas terminadas en NULL.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Uso de cadenas terminadas en NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631785"
---
# <a name="using-null-terminated-strings"></a>Uso de cadenas terminadas en NULL

Las aplicaciones Unicode siempre deben convertir cero a TCHAR cuando se usan cadenas terminadas en NULL. El código 0x0000 es el terminador de cadena Unicode para una cadena terminada en NULL. Un solo byte nulo no es suficiente para este código, ya que muchos caracteres Unicode contienen bytes null como el byte alto o el byte bajo. Un ejemplo es la letra A, para la que se muestra el código de 0x0041.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



