---
title: Administrador de categorías de componentes
description: Administrador de categorías de componentes
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486771"
---
# <a name="the-component-categories-manager"></a>Administrador de categorías de componentes

Para facilitar el control de las categorías de componentes y garantizar la coherencia del registro, el sistema proporciona el administrador de categorías de componentes, un objeto COM con un CLSID de CLSID \_ StdComponentCategoriesMgr. Este objeto COM proporciona las siguientes interfaces:

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) proporciona métodos para obtener información sobre las categorías implementadas o que requiere una determinada clase y proporciona información acerca de las categorías registradas en un equipo determinado.

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) proporciona métodos para registrar y anular el registro de la información de categorías de componentes en el registro. Esto incluye los nombres legibles de las categorías y las categorías implementadas o requeridas por un componente o clase determinados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociar iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> </dl>

 

 




