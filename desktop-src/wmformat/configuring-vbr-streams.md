---
title: Configuración de Secuencias VBR
description: Configuración de Secuencias VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- streams,configuring VBR streams
- streams,variable bit rate (VBR)
- velocidad de bits variable (VBR),streams
- VBR (velocidad de bits variable),streams
- streams,IWMPropertyVault (interfaz)
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251523"
---
# <a name="configuring-vbr-streams"></a>Configuración de Secuencias VBR

Puede usar la codificación de velocidad de bits variable (VBR) para generar secuencias de alta calidad para archivos locales o para descargar y reproducir. Hay tres opciones para VBR: basadas en la calidad (un paso), sin restricciones (dos pases) y restringidas (dos pases). Para obtener más información sobre los tipos de codificación VBR, vea Codificación de velocidad [de bits variable (VBR).](variable-bit-rate--vbr--encoding.md)

Puede configurar la codificación de VBR en un perfil estableciendo propiedades con la [**interfaz IWMPropertyVault.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) En la tabla siguiente se describen las propiedades utilizadas para configurar la codificación vbr.



| Propiedad                     | Descripción                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszVBREnabled**         | Valor booleano. Establezca en True para usar la codificación VBR.                                                   |
| **g \_ wszVBRQuality**         | **Valor DWORD.** Establezca en el nivel de calidad deseado (de 1 a 100) para la codificación VBR basada en calidad.      |
| **g \_ wszVBRBitrateMax**      | **Valor DWORD.** Establezca en la velocidad de bits máxima, en bits por segundo, para la codificación VBR restringida.   |
| **g \_ wszVBRBufferWindowMax** | **Valor DWORD.** Se establece en la ventana de búfer máxima, en milisegundos, para la codificación de VBR restringida. |



 

En las secciones siguientes se describe cómo usar los diferentes tipos de codificación de velocidad de bits variable.



| Sección                                                              | Descripción                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Para configurar Quality-Based VBR](to-configure-quality-based-vbr.md) | Describe cómo usar la codificación de velocidad de bits variable basada en un nivel de calidad estático.                                   |
| [Para configurar VBR sin restricciones](to-configure-unconstrained-vbr.md) | Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media objetivo sin un valor máximo explícito. |
| [Para configurar VBR restringido](to-configure-constrained-vbr.md)     | Describe cómo usar la codificación de velocidad de bits variable basada en una velocidad de bits media de destino y un valor máximo explícito.     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




