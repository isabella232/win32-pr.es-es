---
title: Licencias
description: Licencias
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567745"
---
# <a name="licensing"></a>Licencias

Para insertar controles con licencia correctamente, ActiveX contenedores de controles deben usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) en lugar de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Varias funciones auxiliares de creación y carga de OLE [**(OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) y [**CoCreateInstance)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)llaman explícitamente a **IClassFactory** y no a **IClassFactory2** y, por tanto, no se pueden usar para crear ni cargar controles de ActiveX con licencia. ActiveX contenedores de controles deben crear y cargar explícitamente ActiveX controles mediante **IClassFactory2**.

 

 