---
description: Las Windows networking devuelven WN SUCCESS si se ejecuta correctamente o devuelven un valor distinto de cero único si la función encuentra \_ un error. Además, devuelven información de error extendida mediante WNetSetLastError y SetLastError.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Devolver valores al MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbbb33a1666252178bd6cfb3c2fca33581149dfdab9e16512b60f82875719018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918901"
---
# <a name="returning-values-to-the-mpr"></a>Devolver valores al MPR

Las Windows networking devuelven WN SUCCESS si se ejecuta correctamente o devuelven un valor distinto de cero único si la función encuentra \_ un error. Además, devuelven información de error extendida [**mediante WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) y [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror).

Para admitir el comportamiento anterior, las funciones del proveedor de red no deben llamar a [**SetLastError antes**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) de volver. Esto se debe a que MPR llama **a SetLastError para** las funciones de la API del proveedor de red después de que vuelvan. Si los proveedores de red llaman **directamente a SetLastError,** realizarán llamadas de función redundantes. Las funciones del proveedor de red simplemente deben devolver un código de error. Los códigos de error se especifican en la descripción de la función o [valores devueltos.](network-security-return-values.md) Además, las funciones del proveedor de red pueden devolver cualquier código [de error del sistema,](../debug/system-error-codes.md)como memoria insuficiente. La única excepción [**es NPGetCaps,**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)que debe devolver una máscara que indica las funciones admitidas por el proveedor de red.

Si una función de proveedor de red necesita devolver información de error extendida, debe llamar a [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora). Esta función la proporciona el Windows operativo para su uso por parte de los proveedores de red. Cuando el proveedor llama **a WNetSetLastError,** puede establecer una cadena que contiene información adicional sobre el error. Esta información se almacena por subproceso. Esto es análogo a [**SetLastError para**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) Windows aplicaciones. El Windows operativo llama a **WNetSetLastError** para comprobar si hay una cadena almacenada mediante **WNetSetLastError** y, si se encuentra, devuelve la información de error extendida a la aplicación que realiza la llamada que inició la solicitud de red.

> [!Note]  
> El prefijo WNet de [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) es confuso, ya que esta API, a diferencia de **WNetSetLastError,** no forma parte del conjunto Windows API para redes datos. **WNetSetLastError** está pensado para su uso únicamente por parte de proveedores de red. El nombre, **WNetSetLastError**, se conserva por compatibilidad con los proveedores existentes.

 

 

 
