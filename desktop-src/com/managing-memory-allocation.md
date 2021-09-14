---
title: Administración de la asignación de memoria
description: Administración de la asignación de memoria
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249224"
---
# <a name="managing-memory-allocation"></a>Administración de la asignación de memoria

En COM, muchos métodos de interfaz, si no la mayoría, se llaman mediante código escrito por una organización de programación e implementado por código escrito por otra. Muchos de los parámetros y valores devueltos de estas funciones son de tipos que se pueden pasar por valor. Sin embargo, a veces es necesario pasar estructuras de datos para las que no es el caso, por lo que es necesario que tanto el llamador como el llamador tengan una directiva de asignación y desatribución compatible. COM define una convención universal para la asignación de memoria, porque es más razonable que definir reglas caso por caso y para que la implementación de llamadas a procedimiento remoto COM pueda administrar correctamente la memoria.

Los métodos de una interfaz COM siempre proporcionan administración de memoria de punteros a la interfaz mediante una llamada a las funciones [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) que se encuentran en la interfaz [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de la que derivan todas las demás interfaces COM. (Consulte [Reglas para administrar recuentos de referencias](rules-for-managing-reference-counts.md) para obtener más información).

En esta sección solo se describe cómo asignar memoria a parámetros que no se pasan por valor, no punteros a interfaces, sino cosas más rutinarias como cadenas, punteros a estructuras, etc.

Para obtener más información, vea los temas siguientes:

-   [Asignador de memoria OLE](the-ole-memory-allocator.md)
-   [Reglas de administración de memoria](memory-management-rules.md)
-   [Depuración de asignaciones de memoria](debugging-memory-allocations.md)

 

 