---
description: La función DuplicateHandle crea un identificador duplicado que se puede usar en otro proceso especificado.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082984"
---
# <a name="object-duplication"></a>Duplicación de objetos

La función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crea un identificador duplicado que se puede usar en otro proceso especificado. Este método de compartir identificadores de objetos es más complejo que el uso de objetos con nombre o herencia. Requiere la comunicación entre el proceso de creación y el proceso en el que se duplica el controlador. La información necesaria (el identificador de proceso y el valor de identificador) se puede comunicar mediante cualquiera de los métodos de comunicación entre procesos, como canalizaciones con nombre o memoria compartida con nombre.

 

 
