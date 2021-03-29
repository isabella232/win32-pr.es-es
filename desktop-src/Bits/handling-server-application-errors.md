---
title: Control de errores de aplicación de servidor
description: Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773392"
---
# <a name="handling-server-application-errors"></a>Control de errores de aplicación de servidor

Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200. Si la aplicación no devuelve 200, el cliente de BITS utiliza el código de error para determinar si el error es un error transitorio o un error grave.

Todos los códigos de error 3xx son errores transitorios excepto 300-305 y 307, que son errores irrecuperables. Todos los códigos de error 4xx son errores irrecuperables, excepto 408 y 409, que son errores transitorios. Todos los códigos de error 5xx son errores transitorios excepto 501 y 505, que son errores irrecuperables. El resto de códigos HTTP se consideran errores transitorios. Tenga en cuenta que un código de error 403 es el único código de error que impide que BITS publique el archivo de carga en la aplicación de servidor de nuevo.

Para recuperar el error, llame al método [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . El contexto de error será la \_ aplicación remota de contexto de error de BG \_ \_ \_ .

 

 




