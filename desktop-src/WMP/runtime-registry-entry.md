---
title: Entrada del Registro en tiempo de ejecución
description: Entrada del Registro en tiempo de ejecución
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Reproductor de Windows Media,entradas del Registro en tiempo de ejecución
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,registry
- registry,file name extensions
- registro, entradas en tiempo de ejecución
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- entradas del Registro en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677cb5edb397089a7c432e2464a4d38d6cf5f4c4948070bbef1b1b9cb5c5bebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933685"
---
# <a name="runtime-registry-entry"></a>Entrada del Registro en tiempo de ejecución

Cuando Reproductor de Windows Media encuentra una extensión de nombre de archivo personalizada, busca una subclave del Registro que coincida con la extensión. La subclave se describe en [File Name Extension Registry Configuración](file-name-extension-registry-settings.md). Una de las entradas del Registro que pueden aparecer en la subclave de la extensión es la entrada **runtime.**

La **entrada Runtime** especifica la tecnología subyacente que Reproductor de Windows Media usar para reproducir o convertir archivos multimedia digitales que tienen la extensión personalizada. La **entrada Runtime** tiene el formato siguiente.



|   Nombre   |   Tipo         |   Valor                                                       |
|----------|----------------|---------------------------------------------------------------|
| Tiempo de ejecución  | **REG \_ DWORD** | Entero positivo que identifica la tecnología subyacente. |



 

El valor de la entrada **runtime** debe ser uno de los siguientes.



| **Valor (decimal)** | **Descripción**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Representación mediante el SDK Windows Media Format.                                                 |
| 7                   | Representar mediante Microsoft DirectShow.                                                         |
| 13                  | Convierta el archivo mediante el complemento de conversión especificado. Requiere Reproductor de Windows Media 11. |



 

Los **valores de** entrada del Registro en tiempo de ejecución 6 y 7 son compatibles Reproductor de Windows Media serie 9 y versiones posteriores. El valor 13 es compatible con Reproductor de Windows Media 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Subclave ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Extensión de nombre de archivo Configuración**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




