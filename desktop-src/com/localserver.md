---
title: LocalServer
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Com de clave del Registro LocalServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314b27bcb32dbdce95ffe70d4eaf41183dffd1f554342a8212b03f27058e266c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918565"
---
# <a name="localserver"></a>LocalServer

Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG SZ** que especifica la ruta de acceso completa y puede incluir cualquier argumento de línea de comandos.

COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y buscar la marca -Embedding.

Para ejecutar un servidor de objetos COM en un espacio de memoria independiente, cambie el valor de **LocalServer** como se muestra a continuación:

**cmd /c start /separate** *path.exe**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




