---
description: Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C (malloc, free, etc.) y C++ (nuevo, eliminar, etc.).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funciones de la biblioteca estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666687"
---
# <a name="standard-c-library-functions"></a>Funciones de la biblioteca estándar de C

Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C (**malloc**, **Free**, etc.) y C++ (**nuevo**, **eliminar**, etc.). Las funciones de la biblioteca en tiempo de ejecución de C no tienen los posibles problemas que tienen en Windows de 16 bits. La administración de memoria ya no es un problema porque el sistema es libre de administrar la memoria moviendo páginas de la memoria física sin afectar a las direcciones virtuales. Del mismo modo, la distinción entre punteros Near y Far ya no es relevante. Por lo tanto, puede usar las funciones de la biblioteca estándar de C para la administración de memoria. Sin embargo, las funciones de administración de memoria proporcionan funcionalidad que no está disponible en la biblioteca en tiempo de ejecución de C.

 

 



