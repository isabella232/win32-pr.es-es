---
title: Memoria huérfana
description: Si la aplicación distribuida utiliza un parámetro \ in, out, Unique \ o \ in, out, PTR, el lado servidor de la aplicación puede cambiar el valor del parámetro Pointer a NULL.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676483"
---
# <a name="memory-orphaning"></a>Memoria huérfana

Si la aplicación distribuida utiliza un \[ parámetro [de puntero in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [Unique](/windows/desktop/Midl/unique) \] o \[ **in**, **out**, [ptr](/windows/desktop/Midl/ptr) \] , el lado servidor de la aplicación puede cambiar el valor del parámetro Pointer a NULL. Cuando el servidor devuelve posteriormente el valor null al cliente, la memoria a la que hace referencia el puntero antes de la llamada a procedimiento remoto todavía está presente en el lado cliente, pero ya no es accesible desde ese puntero (excepto en el caso de un puntero completo con alias). Se dice que esta memoria está *huérfana*. Esto también se denomina pérdida de *memoria*. La memoria huérfana que se repite en el cliente hace que el cliente se quede sin recursos de memoria disponibles.

También se puede eliminar la memoria cuando el servidor cambia un puntero incrustado a un valor null. Por ejemplo, si el parámetro apunta a una estructura de datos compleja, como un árbol, el lado servidor de la aplicación puede eliminar nodos del árbol y establecer punteros dentro del árbol en NULL.

Otra situación que puede conducir a una fuga de memoria implica que las matrices que contienen punteros sean compatibles, distintas y abiertas. Cuando la aplicación de servidor modifica el parámetro que especifica el tamaño de la matriz o el intervalo transmitido para que represente un valor más pequeño, el código auxiliar usa los valores más pequeños para liberar memoria. Los elementos de matriz con índices mayores que el parámetro de tamaño son huérfanos. La aplicación debe liberar elementos fuera del intervalo transmitido.

 

 