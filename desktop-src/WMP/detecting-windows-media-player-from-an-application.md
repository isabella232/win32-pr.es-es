---
title: Detección de Media Player de Windows desde una aplicación
description: Detección de Media Player de Windows desde una aplicación
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, detectar desde aplicaciones
- detección de Media Player de Windows desde aplicaciones
- registro, detección de Media Player de Windows desde aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695450"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Detección de Media Player de Windows desde una aplicación

Puede determinar qué versión de Windows Media Player está instalada mediante la comprobación de la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Active Setup \\ componentes instalados**

Para Windows Media Player 6,4, consulte la clave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

En Windows Media Player 7 o versiones posteriores, consulte la clave **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.

En cualquiera de estas claves, si el **IsInstalled**<dl> <dt>

Tipo de datos
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo de datos
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir el software de Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




