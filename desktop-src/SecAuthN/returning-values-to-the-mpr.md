---
description: Las funciones de red de Windows devuelven el \_ éxito de WN si se ejecuta correctamente o devuelven un valor distinto de cero único si la función encuentra un error. Además, devuelven información de error extendida mediante WNetSetLastError y SetLastError.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Devolver valores al MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c96a5636f57d5c926af4e43e676f0b6db75d164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001853"
---
# <a name="returning-values-to-the-mpr"></a>Devolver valores al MPR

Las funciones de red de Windows devuelven el \_ éxito de WN si se ejecuta correctamente o devuelven un valor distinto de cero único si la función encuentra un error. Además, devuelven información de error extendida mediante [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) y [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror).

Para admitir el comportamiento anterior, las funciones de proveedor de red no deben llamar a [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) antes de devolver. Esto se debe a que el MPR llama a **SetLastError** para las funciones de la API de proveedor de red después de que devuelvan. Si los proveedores de red llaman directamente a **SetLastError** , estarán realizando llamadas a funciones redundantes. Las funciones de proveedor de red simplemente deben devolver un código de error. Los códigos de error se especifican en la descripción de la función o [los valores devueltos](network-security-return-values.md). Además, las funciones de proveedor de red pueden devolver cualquier [código de error del sistema](../debug/system-error-codes.md), como memoria insuficiente. La única excepción es [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps), que debe devolver una máscara que indica las funciones admitidas por el proveedor de red.

Si una función de proveedor de red necesita devolver información de error extendida, debe llamar a [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora). Esta función la proporciona el sistema operativo Windows para su uso por parte de proveedores de red. Cuando el proveedor llama a **WNetSetLastError**, puede establecer una cadena que contenga información adicional sobre el error. Esta información se almacena por subproceso. Esto es análogo a [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) para aplicaciones Windows. El sistema operativo Windows llama a **WNetSetLastError** para buscar una cadena almacenada mediante **WNetSetLastError** y, si se encuentra, devuelve la información de error extendida a la aplicación que realiza la llamada que inició la solicitud de red.

> [!Note]  
> El prefijo de WNet de [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) es engañoso, ya que esta API, a diferencia de **WNetSetLastError**, no forma parte del conjunto de API de redes de Windows. **WNetSetLastError** está pensado para su uso únicamente por parte de proveedores de red. El nombre, **WNetSetLastError**, se conserva por compatibilidad con los proveedores existentes.

 

 

 
