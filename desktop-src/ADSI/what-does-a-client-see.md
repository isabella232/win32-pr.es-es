---
title: ¿Qué ve un cliente?
description: En este tema se enumeran las formas en que un cliente ve los datos ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- ADSI de extensiones, ¿qué ve un cliente?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970376"
---
# <a name="what-does-a-client-see"></a>¿Qué ve un cliente?

-   Un cliente ve ADSI y todos sus objetos de extensión como un objeto .
-   Un cliente ADSI ve una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que controla todas las interfaces duales y de distribución del objeto, independientemente de si el agregador implementa la interfaz dual o de distribución en el proveedor o mediante una extensión. Consulte Resolución [de conflictos de nombre de](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)función o propiedad en Automation en Extensiones .
-   ADSI no expone información de tipo a través de los métodos [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch::GetTypeInfoCount.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) ADSI proporciona información de tipos a través de la biblioteca de tipos.

 

 