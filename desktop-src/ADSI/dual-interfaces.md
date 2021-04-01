---
title: Interfaces duales (ADSI)
description: Use las interfaces COM para tener acceso a las propiedades y los métodos en cualquier objeto ADSI de proveedor.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793791"
---
# <a name="dual-interfaces-adsi"></a>Interfaces duales (ADSI)

Use las interfaces COM para tener acceso a las propiedades y los métodos en cualquier objeto ADSI de proveedor. Una propiedad de solo lectura se asigna a una entrada de interfaz del **formulario \_ <PropertyName> Get**. Una propiedad de lectura y escritura se asigna a dos entradas de interfaz del formulario **Get \_ <PropertyName>** y **Put \_ <PropertyName>**.

Todos los métodos de una interfaz COM deben:

-   Devuelve un valor HRESULT para indicar si la operación se ha realizado correctamente o no. El tipo **HRESULT** se describe en la especificación com.
-   En las llamadas a **QueryInterface**, se devuelve **E \_ nointerface** para interfaces no implementadas.
-   Devuelve **E \_ NOTIMPL** para los métodos no implementados en interfaces que, de otro modo, se implementan.
-   **No se \_ \_ \_ \_ admite la propiedad** Return de E ADS para las propiedades de interfaz que no se admiten.

Para conservar la compatibilidad con los controladores de automatización, todos los parámetros y tipos devueltos deben estar dentro del subconjunto definido por el tipo de datos de la variante de automatización. Para obtener más información, consulte **Variant** y **VARIANTARG** en el kit de desarrollo de software (SDK) de la plataforma.

Un objeto de Active Directory de proveedor puede exponer interfaces que usan tipos de datos distintos de los del subconjunto **Variant** . Sin embargo, los controladores de automatización como Visual Basic no pueden llamar a esas interfaces. La mayoría de las interfaces del proveedor ADSI derivan de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y se pueden usar como punteros de interfaz **IDispatch** . Sin embargo, las interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)y [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) no se derivan de **IDispatch**.

 

 