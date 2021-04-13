---
title: Interfaces de almacenamiento
description: Interfaces de almacenamiento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533537"
---
# <a name="storage-interfaces"></a>Interfaces de almacenamiento

Los contenedores de control deben ser capaces de admitir controles que implementan [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Opcionalmente, un contenedor puede admitir cualquier otra interfaz de persistencia como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))y [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para los controles que proporcionan compatibilidad.

Una vez que un contenedor de controles ActiveX ha elegido e inicializado una interfaz de almacenamiento que se va a usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), la interfaz de almacenamiento seguirá siendo la interfaz de almacenamiento principal mientras dure el control, es decir, el control permanecerá en posesión del almacenamiento. Esto no impide que el contenedor se guarde en otras interfaces de almacenamiento.

No es necesario que los contenedores de controles ActiveX admitan un mecanismo de texto de guardar como, por lo que el uso de [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) y el método [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) de la interfaz de contenedor asociada son opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 