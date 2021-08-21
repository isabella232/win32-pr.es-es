---
title: ¿Qué ve un cliente?
description: En este tema se enumeran las formas en que un cliente ve los datos ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- ADSI de extensiones, ¿qué ve un cliente?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d38563de47cfc80bdcf265249bf3e4cf10bc46471e18672221fed8c3047efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082179"
---
# <a name="what-does-a-client-see"></a>¿Qué ve un cliente?

-   Un cliente ve ADSI y todos sus objetos de extensión como un objeto.
-   Un cliente ADSI ve una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que controla todas las interfaces dual y de distribución del objeto, independientemente de si el agregador implementa la interfaz dual o de distribución en el proveedor o mediante una extensión. Consulte Resolución [de conflictos de nombre de función o propiedad en Automation en Extensiones](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI no expone ninguna información de tipo a través de los métodos [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch::GetTypeInfoCount.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) ADSI proporciona información de tipos a través de la biblioteca de tipos.

 

 