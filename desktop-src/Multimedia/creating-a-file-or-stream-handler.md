---
title: Crear un controlador de archivos o secuencias
description: Crear un controlador de archivos o secuencias
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6732c572e390f3401f6e0472659bec7c522189b357b04d8ef7def20a7d9519b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785795"
---
# <a name="creating-a-file-or-stream-handler"></a>Crear un controlador de archivos o secuencias

En una aplicación escrita en el lenguaje de programación C, un controlador de archivos o secuencias normalmente crea una función para cada método. La aplicación tiene acceso a estas funciones a través de una matriz de punteros de función que crea el controlador de secuencias. Una **estructura IAVIStreamVtbl** contiene la matriz de punteros de función. Un controlador de flujo puede asignar cualquier nombre que desee a las funciones que crea para los métodos. La posición del puntero de función en la estructura implica la correspondencia de la función con el método . Por ejemplo, el primer puntero de función de la estructura corresponde al **método QueryInterface.** El controlador de secuencias debe proporcionar todas las funciones de una interfaz.

 

 




