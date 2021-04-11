---
title: Delegación de QueryInterface
description: Delegación de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149653"
---
# <a name="delegation-of-queryinterface"></a>Delegación de QueryInterface

Los controladores que requieren acceso a algunas de las interfaces internas en el administrador del proxy deben pasar por la interfaz [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) . Esto evita que los controladores deleguen y expongan de forma ciega las interfaces internas del agregado fuera del agregado. Estas interfaces incluyen [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Si el controlador desea exponer **IClientSecurity** o **IMultiQI**, debe implementarlos.

En el caso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), si el cliente intenta establecer la seguridad en una interfaz expuesta por el controlador, el controlador debe establecer la seguridad en el proxy de la interfaz de red subyacente.

En el caso de [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), el controlador debe rellenar las interfaces que conoce y, a continuación, reenviar la llamada al administrador de proxy para obtener el resto de las interfaces rellenadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 