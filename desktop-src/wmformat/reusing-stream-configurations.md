---
title: Reutilizar configuraciones de secuencia
description: Reutilizar configuraciones de secuencia
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- secuencias, reutilización de configuraciones
- perfiles, reutilización de configuraciones de secuencias
- reutilizar configuraciones de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685674"
---
# <a name="reusing-stream-configurations"></a>Reutilizar configuraciones de secuencia

A menudo, hay ocasiones en las que desea volver a usar un objeto de configuración de secuencia de un perfil existente. Es posible que tenga perfiles antiguos que necesiten actualización o que necesite un flujo idéntico a uno en un perfil del sistema. Es más fácil reutilizar las configuraciones de streaming que para crear otras nuevas y, a menudo, puede cambiar algunas opciones de configuración para satisfacer sus necesidades en lugar de crear una nueva.

Tenga en cuenta que existen limitaciones en cuanto a cómo puede cambiar las configuraciones de la secuencia. Si cambia la configuración de forma incorrecta, es posible que el perfil no acepte el objeto de configuración de la secuencia. El perfil acepta frecuentemente configuraciones de flujo incorrectas, pero hace que el objeto de escritor rechace el perfil. Tenga en cuenta las siguientes limitaciones y problemas al usar y modificar las configuraciones de flujo existentes.

-   No modifique nunca el contenido de un archivo. prx para cambiar la configuración de la secuencia. Cuando los perfiles se guardan en cadenas XML y se escriben en un archivo. prx, se pueden leer con cualquier editor de texto. Examinar un perfil guardado puede ayudarle a comprender cómo funcionan los perfiles. Sin embargo, nunca debe modificar un archivo. prx de ningún modo. Incluso los cambios aparentemente triviales pueden invalidar el perfil.
-   Varias versiones del códec Windows Media Audio usan las mismas configuraciones de flujo. Si tiene un objeto de configuración de secuencia que está configurado como subtipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAUDIOV7 o WMMEDIASUBTYPE \_ WMAudioV8, el flujo resultante se comprimirá con el códec de Windows Media Audio más reciente. Sin embargo, debe evaluar sus necesidades antes de usar un códec de audio existente. Muchos tipos de archivos se pueden mejorar mediante la actualización a la versión más reciente del códec Windows Media Audio Professional o el códec Windows Media Audio Lossless.
-   No cambie nunca el subtipo de una secuencia para actualizar a un códec nuevo. Cuando se usan los métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para obtener una configuración de flujo, el códec adjunta algunos datos que identifican el formato del flujo de bits. Si cambia el subtipo de un objeto de configuración de una secuencia existente, el subtipo no coincidirá con los datos del códec. El objeto de escritor no aceptará un perfil con una configuración de este tipo de flujo.
-   No modifique la configuración de las configuraciones de secuencias de audio comprimidas. Si los valores de una secuencia de audio no se ajustan a sus necesidades, obtenga una nueva configuración de flujo del códec con los métodos de **IWMCodecInfo3**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Obtención de información de configuración de la secuencia de códecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




