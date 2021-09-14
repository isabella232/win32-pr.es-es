---
title: Configuración de script Secuencias
description: Configuración de script Secuencias
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- streams,configuring script streams
- códecs, configuración de secuencias de script
- secuencias de script, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251534"
---
# <a name="configuring-script-streams"></a>Configuración de script Secuencias

Al igual que todos los tipos de secuencia arbitrarios, las secuencias de script deben tener definida una velocidad de bits y una ventana de búfer. El tipo de medio principal de la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) debe establecerse en Script WMMEDIATYPE. \_

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

 

 




