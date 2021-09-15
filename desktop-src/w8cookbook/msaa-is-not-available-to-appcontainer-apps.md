---
title: MSAA no está disponible para aplicaciones Windows Store
description: MSAA no está disponible para aplicaciones Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247664"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA no está disponible para aplicaciones Windows Store

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


## <a name="description"></a>Descripción

Windows 8 no admite MSAA (Microsoft Active Accessibility) para leer o automatizar datos accesibles desde Windows Store. En Automatización de la interfaz de usuario se debe usar la API de Automatización de la interfaz de usuario (UIA), disponible desde Windows 7. Puesto que no hay ninguna aplicación Windows store, no hay implementaciones existentes que se ven afectadas por este cambio. Esto solo afecta a las nuevas aplicaciones y características escritas para Windows 8. Los desarrolladores todavía pueden usar MSAA para exponer sus datos de accesibilidad. Si el proveedor de aplicaciones Windows Store proporciona datos de MSAA, los clientes de UIA podrán leer y automatizar los datos.

Para simplificar la API para Windows aplicaciones de la Tienda Windows 8, decidimos admitir solo Automatización de la interfaz de usuario como cliente para estas aplicaciones. Los clientes de UIA pueden leer los proveedores de UIA de forma nativa, sin traducción. Los clientes de UIA pueden leer proveedores de MSAA como se traducen a través del proxy de UIA a MSAA. Esto reducirá la carga de pruebas para Windows desarrolladores de aplicaciones de la Tienda.

La eliminación de la compatibilidad con proveedores de MSAA reduciría aún más la matriz de pruebas, pero hay aplicaciones principales que todavía están basadas en MSAA y no queremos que sean inaccesibles.

## <a name="manifestation"></a>Manifestación

Windows Los desarrolladores de aplicaciones de la Tienda no podrán acceder a los detalles de MSAA dentro del modelo de aplicación.

## <a name="solution"></a>Solución

No se deben crear nuevos casos automatizados en MSAA para las características de Windows store.

Cambie las herramientas que ya existen que usan MSAA a UIA si necesitan interactuar con Windows Store. Windows Los desarrolladores de aplicaciones de la tienda deben usar Automatización de la interfaz de usuario API.

## <a name="resources"></a>Recursos

-   [Fundamentos de UI Automation](../winauto/entry-uiauto-win32.md)

 

 