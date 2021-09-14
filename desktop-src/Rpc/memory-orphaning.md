---
title: Huérfano de memoria
description: Si la aplicación distribuida usa un parámetro de puntero \ in, out, unique\ o \ in, out, ptr\, el lado servidor de la aplicación puede cambiar el valor del parámetro de puntero a null.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244449"
---
# <a name="memory-orphaning"></a>Huérfano de memoria

Si la aplicación distribuida usa un parámetro de puntero en , out , unique o en \[ [](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) [](/windows/desktop/Midl/unique) \] \[  **out**, [ptr,](/windows/desktop/Midl/ptr) el lado servidor de la aplicación puede cambiar el valor del parámetro de puntero \] a null. Cuando el servidor devuelve posteriormente el valor NULL al cliente, la memoria a la que hace referencia el puntero antes de la llamada a procedimiento remoto sigue estando presente en el lado cliente, pero ya no es accesible desde ese puntero (excepto en el caso de un puntero completo con alias). Se dice que esta memoria está *huérfana.* Esto también se denomina pérdida *de memoria.* La huérfana repetida de memoria en el cliente hace que el cliente se queme de los recursos de memoria disponibles.

La memoria también puede quedar huérfana cada vez que el servidor cambia un puntero incrustado a un valor NULL. Por ejemplo, si el parámetro apunta a una estructura de datos compleja como un árbol, el lado servidor de la aplicación puede eliminar nodos del árbol y establecer punteros dentro del árbol en NULL.

Otra situación que puede provocar una pérdida de memoria implica matrices compatibles, variables y abiertas que contienen punteros. Cuando la aplicación de servidor modifica el parámetro que especifica el tamaño de la matriz o el intervalo transmitido para que represente un valor más pequeño, los códigos auxiliares usan los valores más pequeños para liberar memoria. Los elementos de matriz con índices mayores que el parámetro size están huérfanos. La aplicación debe liberar elementos fuera del intervalo transmitido.

 

 