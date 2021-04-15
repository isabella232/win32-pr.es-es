---
title: Ver o modificar la señal de música (desusado)
description: Ver o modificar la señal de música (desusado)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- SDK de Windows Media Format, visualización o modificación de la señal de música
- Administración de derechos digitales (DRM), visualización o modificación de la señal de música
- DRM (administración de derechos digitales), visualización o modificación de la señal de música
- Microsoft Secure audio Path (SAP), visualización o modificación de la señal de música
- Ruta de acceso de audio seguro (SAP), visualización o modificación de la señal de música
- SAP (ruta de audio segura), visualización o modificación de la señal de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695452"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Ver o modificar la señal de música (desusado)

En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.

En el modelo de Microsoft Secure audio Path (SAP), las aplicaciones no pueden modificar la música protegida de ningún modo. Por ejemplo, cuando una aplicación intenta interceptar una señal de música, la señal suena como ruido aleatorio. Como resultado, las aplicaciones que normalmente modifican señales (como un ecualizador) no pueden cambiar el sonido de la música.

Algunas aplicaciones simplemente ven una señal de música. Por ejemplo, algunas aplicaciones muestran luces intermitentes en el tiempo con la señal de música, pero no la modifican. Para dar cabida a las aplicaciones que ven las señales, una pequeña parte de la música se descifra y se pasa sin cifrar con el contenido cifrado. La señal resultante es muy deficiente (peor que la calidad de teléfono), pero puede ser suficiente para las aplicaciones que ven señales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ruta de acceso de audio seguro de Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




