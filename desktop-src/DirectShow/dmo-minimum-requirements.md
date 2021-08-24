---
description: DMO Requisitos mínimos
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO Requisitos mínimos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc4f664d32112512120f2f20687051a0bff193e00adb7ad595e6975c522fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749145"
---
# <a name="dmo-minimum-requirements"></a>DMO Requisitos mínimos

Cada DMO debe cumplir los siguientes requisitos mínimos:

-   Debe admitir la agregación.
-   Debe exponer la [**interfaz IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)
-   El modelo de subprocesos debe ser "both". Las DDO deben funcionar correctamente en un entorno sin subprocesos.

Las DDO de efecto audio deben admitir [**la interfaz IMediaObjectInPlace,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) para su uso en DirectObject y DirectSound.

Las interfaces siguientes se documentan en otra parte, pero son útiles para muchas DDO. Sin embargo, no son necesarias.

-   **ISpecifyPropertyPages**, **IPropertyPage:** estas interfaces permiten que un DMO proporcione una página de propiedades para que el usuario establezca propiedades.
-   **IPersistStream:** esta interfaz permite al DMO guardar su estado en un almacenamiento persistente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression:**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)estas interfaces permiten a un cliente configurar los valores de compresión y formato de salida de un codificador. (Estas dos interfaces forman parte de la API DirectShow, pero también se recomiendan para las DDO).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



