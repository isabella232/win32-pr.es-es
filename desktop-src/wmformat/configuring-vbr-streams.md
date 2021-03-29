---
title: Configuración de secuencias VBR
description: Configuración de secuencias VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- streams, interfaz IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994940"
---
# <a name="configuring-vbr-streams"></a>Configuración de secuencias VBR

Puede usar la codificación de velocidad de bits variable (VBR) para generar secuencias de alta calidad para archivos locales o para descargar y reproducir. Hay tres opciones para VBR: basado en la calidad (un paso), sin restricciones (dos pasos) y restringido (dos pasos). Para obtener más información sobre los tipos de codificación VBR, consulte [codificación de velocidad de bits variable (VBR)](variable-bit-rate--vbr--encoding.md).

Para configurar la codificación VBR en un perfil, establezca las propiedades con la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) . En la tabla siguiente se describen las propiedades que se usan para configurar la codificación VBR.



| Propiedad                     | Descripción                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszVBREnabled**         | Valor booleano. Establézcalo en true para usar la codificación VBR.                                                   |
| **g \_ wszVBRQuality**         | Valor **DWORD** . Se establece en el nivel de calidad deseado (de 1 a 100) para la codificación VBR basada en la calidad.      |
| **g \_ wszVBRBitrateMax**      | Valor **DWORD** . Se establece en la velocidad de bits máxima, en bits por segundo, para la codificación VBR restringida.   |
| **g \_ wszVBRBufferWindowMax** | Valor **DWORD** . Se establece en la ventana del búfer máximo, en milisegundos, para la codificación VBR restringida. |



 

En las secciones siguientes se describe cómo usar los distintos tipos de codificación de velocidad de bits variable.



| Sección                                                              | Descripción                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Para configurar Quality-Based VBR](to-configure-quality-based-vbr.md) | Describe cómo usar la codificación de velocidad de bits variable basada en un nivel de calidad estático.                                   |
| [Para configurar una VBR sin restricciones](to-configure-unconstrained-vbr.md) | Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media de destino sin un valor de pico explícito. |
| [Para configurar una VBR restringida](to-configure-constrained-vbr.md)     | Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media de destino y un valor máximo explícito.     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




