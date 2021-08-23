---
description: El tipo de medio (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva. Un dispositivo determinado podría ser capaz de controlar solo un tipo de medio o podría tratar con una variedad de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de soporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf79b97adb9df491aef1ff86be62fb838246c85a45b5ce251f5c0e88df5814f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002893"
---
# <a name="media-type"></a>Tipo de soporte

El *tipo de* medio (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva. Un dispositivo determinado podría ser capaz de controlar solo un tipo de medio o podría tratar con una variedad de tipos.

Los proveedores de servicios exponen el tipo de medio o los tipos admitidos por los dispositivos que controlan. Las aplicaciones consultan el tipo de medio y, a continuación, usan esta información para seleccionar una dirección adecuada en la que iniciar una sesión. La respuesta de la aplicación a una sesión ofrecida también se puede basar en el tipo de medio.

Una sesión de comunicaciones determinada, o llamada, puede implicar varios tipos de medios. Para obtener más información, vea Tipo de medio para una sesión.

**TAPI 2.x:** Vea [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **miembro dwAvailableMediaModes** de la estructura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a la que *apunta lpAddressCaps*, CONSTANTES [LINEMEDIAMODE \_](./linemediamode--constants.md).

**TAPI 3.x:** Vea [**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ Constants](tapimediatype--constants.md).
