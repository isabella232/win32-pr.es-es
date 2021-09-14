---
description: DMO Requisitos mínimos
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO Requisitos mínimos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375246"
---
# <a name="dmo-minimum-requirements"></a>DMO Requisitos mínimos

Cada DMO debe cumplir los siguientes requisitos mínimos:

-   Debe admitir la agregación.
-   Debe exponer la [**interfaz IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)
-   El modelo de subprocesos debe ser "ambos". Las DDO deben funcionar correctamente en un entorno de subproceso libre.

Las DDO de efecto audio deben admitir [**la interfaz IMediaObjectInPlace,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) para su uso en DirectObject y Direct Sound.

Las interfaces siguientes se documentan en otra parte, pero son útiles para muchas DDO. Sin embargo, no son necesarias.

-   **ISpecifyPropertyPages**, **IPropertyPage:** estas interfaces permiten a DMO proporcionar una página de propiedades para que el usuario establezca propiedades.
-   **IPersistStream:** esta interfaz permite al DMO guardar su estado en el almacenamiento persistente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression:**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)estas interfaces permiten a un cliente configurar el formato de salida y la compresión de un codificador. (Estas dos interfaces forman parte de la API DirectShow, pero también se recomiendan para las DDO).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



