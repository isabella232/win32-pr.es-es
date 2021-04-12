---
description: Información general sobre el registro de errores
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Información general sobre el registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152285"
---
# <a name="overview-of-error-logging"></a>Información general sobre el registro de errores

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para proporcionar a las aplicaciones la máxima flexibilidad en el control de errores, los [servicios de edición de DirectShow](directshow-editing-services.md) usan un mecanismo de devolución de llamada. La aplicación implementa un método para registrar un error. En tiempo de ejecución, si se produce un error, DES llama al método que ha proporcionado. El método toma parámetros que describen el error. Lo que hace el método con esta información depende de usted. No obstante, debe devolver lo más rápido posible, o podría interferir con la ejecución del programa.

El método de devolución de llamada de registro de errores se encuentra en una interfaz COM, [**IAMErrorLog**](iamerrorlog.md). La aplicación debe implementar esta interfaz. Al igual que todas las interfaces COM, **IAMErrorLog** hereda la interfaz **IUnknown** , por lo que la aplicación también debe implementarla.

Tiene varias opciones para implementar estas interfaces COM. Puede usar el Active Template Library (ATL), que proporciona implementaciones de existencias de los métodos **IUnknown** . DirectShow también proporciona una clase base de C++, [**CUnknown**](cunknown.md), que facilita la implementación de una interfaz com. Para obtener información sobre el uso de **CUnknown**, vea [How to implement IUnknown](how-to-implement-iunknown.md).

En el código de ejemplo de este artículo se define una clase de C++ independiente que implementa **IUnknown** y **IAMErrorLog**. El resultado no es un objeto COM verdadero, porque no admite **CoCreateInstance**. Sin embargo, este enfoque es adecuado para el propósito del ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de registro](logging-errors.md)
</dt> </dl>

 

 



