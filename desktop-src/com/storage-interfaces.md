---
title: Interfaces de almacenamiento
description: Interfaces de almacenamiento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549270"
---
# <a name="storage-interfaces"></a>Interfaces de almacenamiento

Los contenedores de controles deben ser capaces de admitir controles que implementen [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Opcionalmente, un contenedor puede admitir cualquier otra interfaz de persistencia, como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para los controles que proporcionan compatibilidad.

Una vez que un contenedor de controles ActiveX ha elegido e inicializado una interfaz de almacenamiento para usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)etc.), esa interfaz de almacenamiento seguirá siendo la interfaz de almacenamiento principal durante la vigencia del control, es decir, el control permanecerá en posesión del almacenamiento. Esto no impide que el contenedor se guarde en otras interfaces de almacenamiento.

Los contenedores de controles ActiveX no necesitan admitir un mecanismo de guardado como texto, por lo que el uso de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) y la interfaz del lado contenedor [**asociada IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) son opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 