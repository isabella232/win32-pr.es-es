---
description: Lo llama el compilador cuando tiene más de una página de variables locales en la función.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk rutina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538844"
---
# <a name="_chkstk-routine"></a>\_chkstk (rutina)

Lo llama el compilador cuando tiene más de una página de variables locales en la función.

## <a name="remarks"></a>Comentarios

\_Chkstk Routine es una rutina auxiliar para el compilador de C. Para los compiladores x86, se llama a chkstk Routine cuando las variables locales superan los 4 000 bytes; para los \_ compiladores x64, es 8K.

 

 



