---
title: Comprobación de valores devueltos de IAccessible
description: Los desarrolladores de cliente no deben confiar en las macros del Modelo de objetos componentes (COM) SUCCEEDED y FAILED para probar los valores devueltos de IAccessible, ya que los valores distintos de S OK se consideran \_ correctos.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570073"
---
# <a name="checking-iaccessible-return-values"></a>Comprobación de valores devueltos de IAccessible

Los desarrolladores de cliente no deben confiar en las macros del Modelo de objetos componentes (COM) [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) para probar los valores devueltos [**de IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ya que los valores distintos de S OK se consideran \_ correctos. Por ejemplo, un método puede devolver S FALSE, que la macro SUCCEEDED considera correcta, pero sigue recibiendo un puntero \_ **NULL** en un parámetro de salida. 

Los desarrolladores de cliente deben protegerse frente a la posibilidad de que algunos servidores devuelvan códigos de error distintos de los valores documentados. Para que sea seguro, debe asegurarse de que todos los parámetros de salida contienen información válida y cumplen los criterios siguientes:

-   Todos los punteros no son **NULL.**
-   El **miembro vt** de cualquier estructura [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) no es igual que VT \_ EMPTY.

 

 