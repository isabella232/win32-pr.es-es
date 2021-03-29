---
title: Entrada del registro en tiempo de ejecución
description: Entrada del registro en tiempo de ejecución
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, entradas del registro en tiempo de ejecución
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas en tiempo de ejecución
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- entradas del registro en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075967"
---
# <a name="runtime-registry-entry"></a>Entrada del registro en tiempo de ejecución

Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión. La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo. Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada **en tiempo de ejecución** .

La entrada **en tiempo de ejecución** especifica la tecnología subyacente que Windows Media Player puede usar para reproducir o convertir archivos multimedia digitales que tienen la extensión personalizada. La entrada **en tiempo de ejecución** tiene el formato siguiente.



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| **Nombre** | **Tipo**       | **Valor**                                                     |
| Tiempo de ejecución  | **\_valor DWORD reg** | Un entero positivo que identifica la tecnología subyacente. |



 

El valor de la entrada **en tiempo de ejecución** debe ser uno de los siguientes.



| **Valor (decimal)** | **Descripción**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Se representa mediante el SDK de Windows Media Format.                                                 |
| 7                   | Se representa mediante Microsoft DirectShow.                                                         |
| 13                  | Convierte el archivo mediante el complemento de conversión especificado. Requiere Windows Media Player 11. |



 

Los valores 6 y 7 de la entrada del registro **en tiempo de ejecución** son compatibles con Windows Media Player 9 series y versiones posteriores. El valor 13 es compatible con Windows Media Player 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Subclave ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Configuración del registro de la extensión de nombre de archivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




