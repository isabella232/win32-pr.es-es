---
title: IUnknown y herencia de interfaz
description: IUnknown y herencia de interfaz
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaaa45abfb36f82c53615750acaa02d2983c852b974e28adc7fa6bc5493c568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918673"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown y herencia de interfaz

La herencia en COM no significa la reutilización del código. Dado que no hay implementaciones asociadas a interfaces, la herencia de interfaces no significa la herencia de código. Solo significa que el contrato asociado a una interfaz se hereda de una manera de clase base pura-virtual de C++ y se modifica, ya sea agregando nuevos métodos o calificando aún más el uso permitido de métodos. No hay ninguna herencia selectiva en COM. Si una interfaz hereda de otra, incluye todos los métodos que define la otra interfaz.

La herencia se usa con moderación en las interfaces COM predefinidas. Todas las interfaces predefinidas (y las interfaces personalizadas que defina) heredan sus definiciones de la interfaz importante [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que contiene tres métodos vitales: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todos los objetos COM deben implementar la interfaz **IUnknown** porque proporciona los medios, mediante **QueryInterface**, para moverse libremente entre las distintas interfaces que admite un objeto, así como los medios para administrar su duración mediante **AddRef** y **Release**.

Al crear un objeto que admite la agregación [,](aggregation.md)tendría que implementar un conjunto de funciones [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) para todas las interfaces, así como una interfaz **IUnknown** independiente. En cualquier caso, cualquier implementador de objetos implementará **métodos IUnknown.** Consulte la sección [Using and Implementing IUnknown (Uso e implementación de IUnknown)](using-and-implementing-iunknown.md) para obtener más información.

Aunque hay algunas interfaces que heredan sus definiciones de una segunda interfaz además de [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)la mayoría simplemente heredan los métodos de interfaz **IUnknown.** Esto hace que la mayoría de las interfaces sea relativamente compacta y fácil de encapsular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos COM e interfaces](com-objects-and-interfaces.md)
</dt> </dl>

 

 