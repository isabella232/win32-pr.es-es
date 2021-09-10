---
title: Administrador de categorías de componentes
description: Administrador de categorías de componentes
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369684"
---
# <a name="the-component-categories-manager"></a>Administrador de categorías de componentes

Para facilitar el control de las categorías de componentes y garantizar la coherencia del Registro, el sistema proporciona el Administrador de categorías de componentes, un objeto COM con un CLSID de CLSID \_ StdComponentCategoriesMgr. Este objeto COM proporciona las interfaces siguientes:

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**ICatInformation proporciona**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) métodos para obtener información sobre las categorías implementadas o requeridas por una clase determinada y proporciona información sobre las categorías registradas en un equipo determinado.

[**ICatRegister proporciona**](/windows/desktop/api/ComCat/nn-comcat-icatregister) métodos para registrar y anular el registro de la información de categoría de componentes en el registro. Esto incluye los nombres legibles de las categorías y las categorías implementadas o requeridas por un componente o clase determinados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociación de iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidades de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorización por funcionalidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> </dl>

 

 




