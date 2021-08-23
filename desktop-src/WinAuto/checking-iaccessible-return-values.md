---
title: Comprobación de valores devueltos de IAccessible
description: Los desarrolladores de cliente no deben confiar en las macros del Modelo de objetos componentes (COM) SUCCEEDED y FAILED para probar los valores devueltos IAccessible, ya que los valores distintos de S OK se consideran \_ correctos.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1df43a316898ceeb751b114251ca8fbc91a8fc5360558a3929bcc3ecc47cce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759635"
---
# <a name="checking-iaccessible-return-values"></a>Comprobación de valores devueltos de IAccessible

Los desarrolladores de cliente no deben confiar en las macros del Modelo de objetos componentes (COM) [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) para probar los valores devueltos [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ya que los valores distintos de S OK se consideran \_ correctos. Por ejemplo, un método puede devolver S FALSE, que la macro SUCCEEDED considera correcta, pero sigue recibiendo un puntero \_ **NULL** en un parámetro de salida. 

Los desarrolladores de cliente deben protegerse contra la posibilidad de que algunos servidores devuelvan códigos de error distintos de los valores documentados. Para ser seguro, debe asegurarse de que todos los parámetros de salida contienen información válida y cumplen los criterios siguientes:

-   Todos los punteros no son **NULL.**
-   El **miembro vt** de cualquier estructura [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) no es igual a VT \_ EMPTY.

 

 