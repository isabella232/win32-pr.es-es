---
description: Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C (malloc, gratis, y así sucesivamente) y C++ (nuevo, eliminar, y así sucesivamente).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funciones de la biblioteca estándar de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1447a64f00fbd1b4cccf70f7589f267ebba526d66528d7342da68068f81ebfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963215"
---
# <a name="standard-c-library-functions"></a>Funciones de la biblioteca estándar de C

Las aplicaciones pueden usar de forma segura las características de administración de memoria de la biblioteca en tiempo de ejecución de C **(malloc,** **gratis,** y así sucesivamente) y C++**(nuevo,** **eliminar,** y así sucesivamente). Las funciones de la biblioteca en tiempo de ejecución de C no tienen los posibles problemas que tienen en las bibliotecas de 16 Windows. La administración de memoria ya no es un problema porque el sistema es libre de administrar la memoria moviendo páginas de memoria física sin afectar a las direcciones virtuales. De forma similar, la distinción entre punteros cercanos y lejanos ya no es relevante. Por lo tanto, puede usar las funciones estándar de la biblioteca de C para la administración de memoria. Sin embargo, las funciones de administración de memoria proporcionan funcionalidad que no está disponible en la biblioteca en tiempo de ejecución de C.

 

 



