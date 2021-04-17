---
title: Comprobar los valores devueltos de IAccessible
description: Los desarrolladores de cliente no deben confiar en las macros del modelo de objetos componentes (COM) correctas y no pudieron probar los valores devueltos del IAccessible, ya que los valores que no \_ son correctos se consideran correctos.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714417"
---
# <a name="checking-iaccessible-return-values"></a>Comprobar los valores devueltos de IAccessible

Los desarrolladores de cliente no deben confiar en las macros del modelo de objetos componentes (COM) [**correctas**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**no pudieron**](/windows/desktop/api/winerror/nf-winerror-failed) probar los valores devueltos del [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ya que los valores que no \_ son correctos se consideran correctos. Por ejemplo, un método puede devolver S \_ false, lo que se considera que es correcto por la macro **Succeeded** , pero sigue recibiendo un puntero **null** en un parámetro de salida.

Los desarrolladores de cliente deben protegerse frente a la posibilidad de que algunos servidores devuelvan códigos de error distintos de los valores documentados. Para que sea seguro, debe asegurarse de que todos los parámetros de salida contienen información válida y cumplen los siguientes criterios:

-   Todos los punteros no son **null**.
-   El miembro **VT** de cualquier estructura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) no es igual a VT \_ vacío.

 

 