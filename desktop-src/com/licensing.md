---
title: Licencias
description: Licencias
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249308"
---
# <a name="licensing"></a>Licencias

Para insertar controles con licencia correctamente, ActiveX contenedores de controles deben usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) en lugar de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Varias funciones auxiliares de creación y carga de OLE [**(OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) y [**CoCreateInstance)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)llaman explícitamente a **IClassFactory** y no a **IClassFactory2** y, por tanto, no se pueden usar para crear ni cargar controles de ActiveX con licencia. ActiveX contenedores de controles deben crear y cargar explícitamente ActiveX controles mediante **IClassFactory2**.

 

 