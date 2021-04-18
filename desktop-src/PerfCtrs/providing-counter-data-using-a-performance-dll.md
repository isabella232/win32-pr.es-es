---
description: Un servicio, un controlador o una aplicación que desee proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Proporcionar datos de contadores mediante un archivo DLL de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667259"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Proporcionar datos de contadores mediante un archivo DLL de rendimiento

> [!IMPORTANT]
> Debido a las limitaciones de rendimiento y confiabilidad significativas, el método para proporcionar los datos del contador de rendimiento que se describen en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md) para crear nuevos contadores de rendimiento y migrar los contadores de rendimiento existentes para usar ese método también.

Un servicio, un controlador o una aplicación que desee proporcionar datos de contador puede escribir un archivo DLL de rendimiento para proporcionar los datos. Cuando un consumidor consulta datos de rendimiento, el sistema carga la DLL del proveedor en el proceso del consumidor y llama al proveedor para recopilar los datos. Para obtener más información sobre cómo escribir el archivo DLL de rendimiento, consulte [crear un archivo dll de extensión de rendimiento](creating-a-performance-extension-dll.md).

El sistema utiliza el registro para determinar a qué proveedor se debe llamar. Para obtener información sobre cómo registrar el proveedor y los contadores que admite, vea [Agregar contadores de rendimiento](adding-performance-counters.md).

> [!Note]
> Los archivos dll de rendimiento no se admiten en Windows OneCore. Si escribe un componente que se debe ejecutar en Windows OneCore, use el método descrito en [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).
