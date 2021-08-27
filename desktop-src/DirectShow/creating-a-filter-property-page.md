---
description: Crear una página de propiedades de filtro
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Crear una página de propiedades de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d891c42a6cdb2f1c636278a8270fb13a69580697a31fe78f2f3687246f20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108265"
---
# <a name="creating-a-filter-property-page"></a>Crear una página de propiedades de filtro

En esta sección se describe cómo crear una página de propiedades para un filtro DirectShow personalizado, mediante la [**clase CBasePropertyPage.**](cbasepropertypage.md) El código de ejemplo de esta sección muestra todos los pasos necesarios para crear una página de propiedades. En el ejemplo se muestra una página de propiedades para un filtro hipotético de efecto de vídeo que admite una propiedad de saturación. La página de propiedades tiene un control deslizante que el usuario puede mover para ajustar el nivel de saturación del filtro.

Esta sección contiene los siguientes temas:

-   [Paso 1. Definir un mecanismo para establecer la propiedad](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Paso 2. Implementación de ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Paso 3. Compatibilidad con QueryInterface](step-3--support-queryinterface.md)
-   [Paso 4. Crear la página de propiedades](step-4--create-the-property-page.md)
-   [Paso 5. Almacenar un puntero al filtro](step-5--store-a-pointer-to-the-filter.md)
-   [Paso 6. Inicializar el cuadro de diálogo](step-6--initialize-the-dialog.md)
-   [Paso 7. Controlar mensajes de ventana](step-7--handle-window-messages.md)
-   [Paso 8. Aplicar cambios de propiedad](step-8--apply-property-changes.md)
-   [Paso 9. Desconectar la página de propiedades](step-9--disconnect-the-property-page.md)
-   [Paso 10. Compatibilidad con el registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



