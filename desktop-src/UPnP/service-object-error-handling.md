---
title: Control de errores de objetos de servicio
description: Cuando se produce un error en un objeto de servicio, el valor devuelto para la llamada a IDispatch Invoke debe ser DISP E EXCEPTION y el puntero del parámetro pExceptInfo a una estructura EXCEPTINFO de debe \_ \_ rellenarse.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999525"
---
# <a name="service-object-error-handling"></a>Control de errores de objetos de servicio

Cuando se produce un error en un objeto de servicio, el valor devuelto para la llamada [**ADispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) debe ser DISP E EXCEPTION y el puntero del parámetro \_ \_ *pExceptInfo* a una estructura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) de debe rellenarse.

En concreto, el host de dispositivos usa los miembros **bstrSource** y **bstrDescription** de la estructura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) con tecnología UPnP para crear una respuesta de error de UPnP. **bstrSource es** el código de error y **bstrDescription** es la descripción del error.

 

 