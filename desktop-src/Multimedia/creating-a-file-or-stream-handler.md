---
title: Crear un controlador de archivos o secuencias
description: Crear un controlador de archivos o secuencias
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371678"
---
# <a name="creating-a-file-or-stream-handler"></a>Crear un controlador de archivos o secuencias

En una aplicación escrita en el lenguaje de programación C, un controlador de archivos o secuencias normalmente crea una función para cada método. La aplicación tiene acceso a estas funciones a través de una matriz de punteros de función que crea el controlador de secuencias. Una **estructura IAVIStreamVtbl** contiene la matriz de punteros de función. Un controlador de flujo puede asignar cualquier nombre que desee a las funciones que crea para los métodos. La posición del puntero de función en la estructura implica la correspondencia de la función con el método . Por ejemplo, el primer puntero de función de la estructura corresponde al **método QueryInterface.** El controlador de secuencias debe proporcionar todas las funciones de una interfaz.

 

 




