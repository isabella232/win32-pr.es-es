---
title: Controles (COM)
description: Controles
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359597"
---
# <a name="controls-com"></a>Controles (COM)

Un control ActiveX es realmente simplemente otro término para el objeto OLE o más específicamente, un objeto COM. En otras palabras, un control, como mínimo, es un objeto COM que admite la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y también se registra automáticamente. A través de [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , un contenedor puede administrar la duración del control y detectar dinámicamente el alcance completo de la funcionalidad de un control basándose en las interfaces disponibles. Esto permite a un control implementar la menor funcionalidad que necesita, en lugar de admitir un gran número de interfaces que realmente no hacen nada. En Resumen, este requisito mínimo para nada más que **IUnknown** permite que cualquier control sea tan ligero como pueda.

En Resumen, aparte de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y el registro automático, no hay ningún otro requisito para un control. Sin embargo, hay convenciones que se deben seguir sobre lo que significa la compatibilidad de una interfaz en cuanto a la funcionalidad proporcionada por el control por parte del contenedor. En esta sección se describe lo que significa que un control admite realmente una interfaz, así como métodos, propiedades y eventos que un control debe proporcionar como línea base si tiene ocasión de admitir métodos, propiedades y eventos.

Para obtener más información, vea los temas siguientes:

-   [Registro propio para controles](self-registration-for-controls.md)
-   [Compatibilidad con una interfaz](what-support-for-an-interface-means.md)
-   [Interfaces de persistencia](persistence-interfaces.md)
-   [Métodos opcionales en interfaces de control](optional-methods-in-control-interfaces.md)
-   [Opciones del generador de clases](class-factory-options.md)
-   [Exponer propiedades a través de IDispatch](properties.md)
-   [Exponer métodos a través de IDispatch](exposing-methods-through-idispatch.md)
-   [Eventos en controles](events-in-controls.md)
-   [Páginas de propiedades](property-pages.md)
-   [Propiedades de ambiente para controles](ambient-properties-for-controls.md)
-   [Usar la funcionalidad del contenedor](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el contenedor de controles y controles ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




