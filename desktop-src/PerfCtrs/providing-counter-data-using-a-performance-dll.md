---
description: Un servicio, controlador o aplicación que quiera proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Proporcionar datos de contador mediante un archivo DLL de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 165e6a8797c50a22acff1d3cd3ded7f8b06a0ee2a7153300e98e46bea1127f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910315"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Proporcionar datos de contador mediante un archivo DLL de rendimiento

> [!IMPORTANT]
> Debido a limitaciones significativas de rendimiento y confiabilidad, el método para proporcionar datos de contadores de rendimiento que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en Proporcionar datos de contador mediante la versión [2.0 para](providing-counter-data-using-version-2-0.md) crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar también ese método.

Un servicio, controlador o aplicación que quiera proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos. Cuando un consumidor consulta datos de rendimiento, el sistema carga el archivo DLL del proveedor en el proceso del consumidor y llama al proveedor para recopilar los datos. Para obtener más información sobre cómo escribir el archivo DLL de rendimiento, vea [Crear un archivo DLL de extensión de rendimiento.](creating-a-performance-extension-dll.md)

El sistema usa el registro para determinar a qué proveedor llamar. Para obtener información sobre cómo registrar el proveedor y los contadores que admite, vea [Agregar contadores de rendimiento.](adding-performance-counters.md)

> [!Note]
> Los archivos DLL de rendimiento no se admiten en Windows OneCore. Si escribe un componente que debe ejecutarse en Windows OneCore, use el método descrito en Proporcionar datos de contador [mediante la versión 2.0](providing-counter-data-using-version-2-0.md).
