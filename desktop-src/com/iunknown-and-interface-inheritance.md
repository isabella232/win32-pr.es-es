---
title: IUnknown y herencia de interfaz
description: IUnknown y herencia de interfaz
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714475"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown y herencia de interfaz

La herencia en COM no implica la reutilización de código. Dado que no hay implementaciones asociadas a las interfaces, la herencia de interfaz no significa herencia de código. Solo significa que el contrato asociado a una interfaz se hereda en un modo de clase base virtual puro de C++ y se ha modificado, ya sea mediante la adición de nuevos métodos o por la calificación del uso permitido de los métodos. No hay ninguna herencia selectiva en COM. Si una interfaz hereda de otra, incluye todos los métodos que define la otra interfaz.

La herencia se utiliza con moderación en las interfaces COM predefinidas. Todas las interfaces predefinidas (y cualquier interfaz personalizada que defina) heredan sus definiciones de la interfaz importante [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que contiene tres métodos fundamentales: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todos los objetos COM deben implementar la interfaz **IUnknown** porque proporciona los medios, mediante **QueryInterface**, para desplazarse libremente entre las distintas interfaces que admite un objeto, así como los medios para administrar su duración mediante **AddRef** y **Release**.

Al crear un objeto que admita la [agregación](aggregation.md), debería implementar un conjunto de funciones [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) para todas las interfaces, así como una interfaz **IUnknown** independiente. En cualquier caso, cualquier implementador de objetos implementará los métodos **IUnknown** . Vea la sección [uso e implementación de IUnknown](using-and-implementing-iunknown.md) para obtener más información.

Aunque hay algunas interfaces que heredan sus definiciones de una segunda interfaz además de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), la mayoría simplemente hereda los métodos de interfaz **IUnknown** . Esto hace que la mayoría de las interfaces sean relativamente compactas y fáciles de encapsular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 