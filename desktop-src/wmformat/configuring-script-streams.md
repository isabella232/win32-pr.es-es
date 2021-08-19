---
title: Configuración de scripts Secuencias
description: Configuración de scripts Secuencias
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- streams,configuring script streams
- codecs,configuring script streams
- secuencias de script, configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95c4c43fcb29ec2f77dacbf5a66b1c8c36c666d80fd5f5c09779a4ecaf22f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655993"
---
# <a name="configuring-script-streams"></a>Configuración de scripts Secuencias

Al igual que todos los tipos de secuencias arbitrarios, las secuencias de script deben tener definida una velocidad de bits y una ventana de búfer. El tipo de medio principal de la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) debe establecerse en Script WMMEDIATYPE. \_

Las secuencias de script deben tener el miembro **formattype** de **WM MEDIA \_ \_ TYPE** establecido en Script WMFORMAT, lo que indica que el miembro pbFormat apunta a una \_ estructura [**WMSCRIPTFORMAT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) 

Solo hay un tipo de script compatible, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> </dl>

 

 




