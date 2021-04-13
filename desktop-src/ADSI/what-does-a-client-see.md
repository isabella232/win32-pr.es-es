---
title: Qué ve un cliente
description: En este tema se enumeran las formas en que un cliente ve datos ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, qué ve un cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533495"
---
# <a name="what-does-a-client-see"></a>¿Qué ve un cliente?

-   Un cliente ve ADSI y todos sus objetos de extensión como un objeto.
-   Un cliente ADSI ve una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que controla todas las interfaces de distribución y dual en el objeto, independientemente de si el agregador implementa la interfaz dual o de distribución en el proveedor o mediante una extensión. Consulte [resolución de conflictos de nombres de función y propiedad en la automatización en las extensiones](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI no expone ninguna información de tipo a través de los métodos [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) . ADSI proporciona información de tipos a través de la biblioteca de tipos.

 

 