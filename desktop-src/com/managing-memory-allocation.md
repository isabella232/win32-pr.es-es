---
title: Administrar la asignación de memoria
description: Administrar la asignación de memoria
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421487"
---
# <a name="managing-memory-allocation"></a>Administrar la asignación de memoria

En COM, muchos, si no más, se llama a los métodos de interfaz mediante código escrito por una organización de programación y se implementa mediante código escrito por otro. Muchos de los parámetros y valores devueltos de estas funciones son de tipos que se pueden pasar por valor. Sin embargo, a veces es necesario pasar estructuras de datos para las que este no es el caso, por lo que es necesario que el llamador y la llamada tengan una directiva de asignación y desasignación compatible. COM define una Convención universal para la asignación de memoria, porque es más razonable que definir reglas de caso por caso y para que la implementación de llamadas a procedimientos remotos COM pueda administrar correctamente la memoria.

Los métodos de una interfaz COM siempre proporcionan administración de memoria de punteros a la interfaz llamando a las funciones [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) que se encuentran en la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , de la que derivan todas las demás interfaces com. (Consulte [reglas para administrar recuentos de referencias](rules-for-managing-reference-counts.md) para obtener más información).

En esta sección solo se describe cómo asignar memoria para los parámetros que no se pasan por valor, no punteros a las interfaces, sino aspectos más cotidianos, como cadenas, punteros a estructuras, etc.

Para obtener más información, vea los temas siguientes:

-   [Asignador de memoria OLE](the-ole-memory-allocator.md)
-   [Reglas de administración de memoria](memory-management-rules.md)
-   [Depurar asignaciones de memoria](debugging-memory-allocations.md)

 

 