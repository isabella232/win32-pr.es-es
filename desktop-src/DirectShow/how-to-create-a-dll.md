---
description: Cómo crear un archivo DLL de filtro de DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Cómo crear un archivo DLL de filtro de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651434"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Cómo crear un archivo DLL de filtro de DirectShow

En este artículo se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow. Este artículo es una continuación de [cómo implementar IUnknown](how-to-implement-iunknown.md), en el que se describe cómo implementar la interfaz **IUnknown** mediante la derivación del componente de la clase base [**CUnknown**](cunknown.md) .

Este artículo contiene las secciones siguientes.

-   [Generadores de clases y plantillas de generador](class-factories-and-factory-templates.md)
-   [Matriz de plantillas de fábrica](factory-template-array.md)
-   [Funciones DLL](dll-functions.md)

El registro de un filtro DirectShow (en oposición a un objeto COM genérico) requiere algunos pasos adicionales que no se describen en este artículo. Para obtener información sobre cómo registrar filtros, consulte [How to Register DirectShow filters](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow y COM](directshow-and-com.md)
</dt> </dl>

 

 



