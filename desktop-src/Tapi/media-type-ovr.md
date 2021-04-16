---
description: El tipo de medio (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva. Es posible que un dispositivo determinado solo pueda controlar un tipo de medio, o bien que pueda tratar con un intervalo de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de soporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678631"
---
# <a name="media-type"></a>Tipo de soporte

El *tipo de medio* (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva. Es posible que un dispositivo determinado solo pueda controlar un tipo de medio, o bien que pueda tratar con un intervalo de tipos.

Los proveedores de servicios exponen el tipo o los tipos de medios admitidos por los dispositivos que controlan. Las aplicaciones consultan el tipo de medio y, a continuación, usan esta información para seleccionar una dirección adecuada en la que iniciar una sesión. La respuesta de la aplicación a una sesión ofrecida también se puede predicar en el tipo de medio.

Una sesión de comunicaciones determinada, o llamada, puede implicar varios tipos de medios. Para obtener más información, consulte tipo de medio para una sesión.

**TAPI 2. x:** Vea [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), miembro **dwAvailableMediaModes** de la estructura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a la que apunta *lpAddressCaps*, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).

**TAPI 3. x:** Vea [**ITTerminal:: get \_ mediatype**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).
