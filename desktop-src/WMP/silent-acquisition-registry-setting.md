---
title: Configuración del Registro de adquisición silenciosa
description: Configuración del Registro de adquisición silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507965"
---
# <a name="silent-acquisition-registry-setting"></a>Configuración del Registro de adquisición silenciosa

Microsoft Reproductor de Windows Media usa el siguiente valor del Registro para determinar si se debe habilitar la adquisición silenciosa, un estado en el que el reproductor descarga automáticamente los derechos de uso cuando el usuario reproduce o sincroniza contenido protegido.

**HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Preferencias** de Microsoft \\ **MediaPlayer** \\  \\ **SilentAcquisition**

El valor SilentAcquisition tiene el formato siguiente:



| Nombre              | Tipo           | Descripción                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | Establezca este valor en 1 para habilitar la adquisición silenciosa o estabilite en 0 para deshabilitar la adquisición silenciosa. El valor predeterminado es 1. |



 

Para especificar un valor, el usuario puede iniciar  Reproductor de Windows Media, abrir  el cuadro de diálogo Opciones, hacer clic en la pestaña Privacidad y, a continuación, activar o desactive la casilla Descargar derechos de uso automáticamente al reproducir o sincronizar un archivo.  Al activar esta casilla, SilentAcquisition se establece en 1; si desactiva la casilla, esta se establece en 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




