---
title: Configuración del registro de la adquisición silenciosa
description: Configuración del registro de la adquisición silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704726"
---
# <a name="silent-acquisition-registry-setting"></a>Configuración del registro de la adquisición silenciosa

Microsoft Windows Media Player usa el siguiente valor del registro para determinar si se debe habilitar la adquisición silenciosa, un estado en el que el reproductor descarga los derechos de uso automáticamente cuando el usuario reproduce o sincroniza el contenido protegido.

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **MediaPlayer** \\ **Preferences** \\ **SilentAcquisition**

El valor de SilentAcquisition tiene el formato siguiente:



| Nombre              | Tipo           | Descripción                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **\_valor DWORD reg** | Establezca este valor en 1 para habilitar la adquisición silenciosa o establézcalo en 0 para deshabilitar la adquisición silenciosa. El valor predeterminado es 1. |



 

Para especificar un valor, el usuario puede iniciar Windows Media Player, abrir el cuadro de diálogo **Opciones** , hacer clic en la pestaña **privacidad** y, a continuación, activar o desactivar la casilla **descargar los derechos de uso automáticamente al reproducir o sincronizar un archivo** . Al activar esta casilla, se establece SilentAcquisition en 1; al desactivar la casilla, se establece en 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro**](registry-settings.md)
</dt> </dl>

 

 




