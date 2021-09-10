---
title: LocalServer
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Com de clave del Registro LocalServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369467"
---
# <a name="localserver"></a>LocalServer

Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ** que especifica la ruta de acceso completa y puede incluir cualquier argumento de línea de comandos.

COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y comprobar la marca -Embedding.

Para ejecutar un servidor de objetos COM en un espacio de memoria independiente, cambie el valor de **LocalServer** como se muestra a continuación:

**cmd /c start /separate** *path**.exe**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




