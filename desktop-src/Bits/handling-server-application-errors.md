---
title: Control de errores de aplicación de servidor
description: Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005285"
---
# <a name="handling-server-application-errors"></a>Control de errores de aplicación de servidor

Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200. Si la aplicación no devuelve 200, el cliente bits usa el código de error para determinar si el error es transitorio o irrespreso.

Todos los códigos de error 3xx son errores transitorios excepto 300- 305 y 307, que son errores irreales. Todos los códigos de error 4xx son errores irreales, excepto 408 y 409, que son errores transitorios. Todos los códigos de error 5xx son errores transitorios excepto 501 y 505, que son errores irreales. Todos los demás códigos HTTP se consideran errores transitorios. Tenga en cuenta que un código de error 403 es el único código de error que impide que BITS vuelva a publicar el archivo de carga en la aplicación de servidor.

Para recuperar el error, llame al [**método IBackgroundCopyError::GetError.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) El contexto de error será BG \_ ERROR \_ CONTEXT REMOTE \_ \_ APPLICATION.

 

 




