---
description: La función DuplicateHandle crea un identificador duplicado que puede usar otro proceso especificado.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886345"
---
# <a name="object-duplication"></a>Duplicación de objetos

La [**función DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crea un identificador duplicado que puede usar otro proceso especificado. Este método de uso compartido de identificadores de objetos es más complejo que usar objetos con nombre o herencia. Requiere comunicación entre el proceso de creación y el proceso en el que se duplica el identificador. La información necesaria (el valor del identificador y el identificador del proceso) se puede comunicar mediante cualquiera de los métodos de comunicación entre procesos, como canalizaciones con nombre o memoria compartida con nombre.

 

 
