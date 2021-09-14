---
description: Cómo crear un archivo DLL DirectShow filtro de archivos
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Cómo crear un archivo DLL DirectShow filtro de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169909"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Cómo crear un archivo DLL DirectShow filtro de archivos

En este artículo se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow. Este artículo es una continuación de Cómo implementar [IUnknown](how-to-implement-iunknown.md), que describe cómo implementar la interfaz **IUnknown** derivando el componente de la clase base [**CUnknown.**](cunknown.md)

Este artículo contiene las secciones siguientes.

-   [Generadores de clases y plantillas de fábrica](class-factories-and-factory-templates.md)
-   [Matriz de plantillas de fábrica](factory-template-array.md)
-   [Funciones DLL](dll-functions.md)

El registro de DirectShow filtro (en lugar de un objeto COM genérico) requiere algunos pasos adicionales que no se tratan en este artículo. Para obtener información sobre el registro de filtros, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow y COM](directshow-and-com.md)
</dt> </dl>

 

 



