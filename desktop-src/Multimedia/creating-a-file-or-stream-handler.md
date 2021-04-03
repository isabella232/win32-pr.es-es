---
title: Crear un controlador de archivo o secuencia
description: Crear un controlador de archivo o secuencia
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075587"
---
# <a name="creating-a-file-or-stream-handler"></a>Crear un controlador de archivo o secuencia

En una aplicación escrita en el lenguaje de programación C, un controlador de archivo o secuencia normalmente crea una función para cada método. La aplicación tiene acceso a estas funciones a través de una matriz de punteros de función que crea el controlador de flujo. Una estructura **IAVIStreamVtbl** contiene la matriz de punteros de función. Un controlador de flujo puede asignar cualquier nombre que desee a las funciones que crea para los métodos. La posición del puntero de función en la estructura implica la correspondencia de la función con el método. Por ejemplo, el primer puntero de función de la estructura corresponde al método **QueryInterface** . El controlador de flujo debe proporcionar todas las funciones de una interfaz.

 

 




