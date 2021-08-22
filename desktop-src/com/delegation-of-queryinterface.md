---
title: Delegación de QueryInterface
description: Delegación de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501215"
---
# <a name="delegation-of-queryinterface"></a>Delegación de QueryInterface

Los controladores que requieren acceso a algunas de las interfaces internas del administrador de proxy tienen que pasar por la [**interfaz IInternalUnknown.**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) Esto evita que los controladores deleguen y expongan las interfaces internas del agregado fuera del agregado. Estas interfaces incluyen [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) [**e IMultiQI.**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) Si el controlador desea exponer **IClientSecurity** o **IMultiQI,** debe implementarlos por sí mismo.

En el caso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), si el cliente intenta establecer la seguridad en una interfaz que el controlador ha expuesto, el controlador debe establecer la seguridad en el proxy de interfaz de red subyacente.

En el caso de [**IMultiQI,**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)el controlador debe rellenar las interfaces que conoce y, a continuación, reenviar la llamada al administrador de proxy para rellenar el resto de las interfaces.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 