---
title: Detección de Reproductor de Windows Media desde una aplicación
description: Detección de Reproductor de Windows Media desde una aplicación
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Reproductor de Windows Media, detectar desde aplicaciones
- detección de Reproductor de Windows Media desde aplicaciones
- registro, detección de Reproductor de Windows Media desde aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579491"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Detección de Reproductor de Windows Media desde una aplicación

Puede determinar qué versión de Reproductor de Windows Media está instalada comprobando la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Active Setup \\ Installed Components**

Para Reproductor de Windows Media 6.4, vea la clave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

Para Reproductor de Windows Media 7 o posterior, vea la clave **{6BF52A52-394A-11d3-B153-00C04F79FAA6}.**

En cualquiera de estas claves, si **isInstalled**<dl> <dt>

Tipo de datos
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo de datos
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir Reproductor de Windows Media software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




