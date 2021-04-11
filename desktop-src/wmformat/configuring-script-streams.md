---
title: Configurar secuencias de scripts
description: Configurar secuencias de scripts
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flujos, configurar secuencias de scripts
- códecs, configurar secuencias de scripts
- secuencias de comandos, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075595"
---
# <a name="configuring-script-streams"></a>Configurar secuencias de scripts

Al igual que todos los tipos de secuencia arbitrarios, los flujos de scripts deben tener una ventana de velocidad de bits y de búfer definida para ellos. El tipo de medio principal de la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) debe establecerse en el script WMMEDIATYPE \_ .

Los flujos de scripts deben tener el miembro **formatType** de **tipo de \_ medio \_ de WM** establecido en el \_ script WMFORMAT, lo que indica que el miembro **pbFormat** apunta a una estructura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

Solo hay un tipo de script admitido, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> </dl>

 

 




