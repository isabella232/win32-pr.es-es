---
title: Volver a la utilización de configuraciones de flujo
description: Volver a la utilización de configuraciones de flujo
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- streams,reusing configurations
- perfiles, reusar configuraciones de flujo
- volver a la utilización de configuraciones de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ee1a2b51d5a2a659cb24955ab74a5fb285308125b21781c9d42a709d7e4b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110195"
---
# <a name="reusing-stream-configurations"></a>Volver a la utilización de configuraciones de flujo

A menudo hay ocasiones en las que se desea reutilizar un objeto de configuración de flujo desde un perfil existente. Es posible que tenga perfiles antiguos que necesiten actualizarse o que necesite una secuencia idéntica a la de un perfil del sistema. Es más fácil reutilizar las configuraciones de flujo que crear otras nuevas y, a menudo, puede cambiar algunas opciones de una configuración para satisfacer sus necesidades en lugar de crear una completamente nueva.

Tenga en cuenta que hay limitaciones en cómo puede cambiar las configuraciones de flujo. Si cambia la configuración de forma incorrecta, es posible que el perfil no acepte el objeto de configuración de flujo. El perfil acepta con frecuencia configuraciones de secuencia incorrectas, pero hacen que el objeto de escritor rechace el perfil. Tenga en cuenta las siguientes limitaciones y problemas al usar y modificar las configuraciones de flujo existentes.

-   No modifique nunca el contenido de un archivo .prx para cambiar la configuración del flujo. Cuando los perfiles se guardan en cadenas XML y se escriben en un archivo .prx, se pueden leer con cualquier editor de texto. La búsqueda de un perfil guardado puede ayudarle a comprender cómo funcionan los perfiles. Sin embargo, nunca debe modificar un archivo .prx de ninguna manera. Incluso los cambios aparentemente triviales pueden invalidar el perfil.
-   Varias versiones del códec Windows Media Audio usan las mismas configuraciones de secuencia. Si tiene un objeto de configuración de secuencia configurado como subtipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAudioV7 o WMMEDIASUBTYPE WMAudioV8, la secuencia resultante se comprimirá con el códec de audio multimedia de Windows más \_ reciente. Sin embargo, debe evaluar sus necesidades antes de usar un códec de audio existente. Muchos tipos de archivos se pueden mejorar mediante la actualización a la versión más reciente del códec Professional audio multimedia de Windows o al códec sin pérdida de audio multimedia Windows de Windows.
-   Nunca cambie el subtipo de una secuencia para actualizar a un códec nuevo. Cuando se usan los métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para obtener una configuración de secuencia, el códec le adjunta algunos datos que identifican el formato de secuencia de bits. Si cambia el subtipo de un objeto de configuración de secuencia existente, el subtipo no coincidirá con los datos del códec. El objeto de escritor no aceptará un perfil con esta configuración de secuencia.
-   No modifique la configuración de las configuraciones de secuencias de audio comprimidas. Si la configuración de una secuencia de audio no se adapta a sus necesidades, obtenga una nueva configuración de secuencia del códec mediante los métodos de **IWMCodecInfo3**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Obtención de información de configuración de secuencias de códecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




