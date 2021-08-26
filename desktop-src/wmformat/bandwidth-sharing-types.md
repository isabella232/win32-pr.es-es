---
title: Tipos de uso compartido de ancho de banda
description: Tipos de uso compartido de ancho de banda
ms.assetid: 2da15981-65d4-4d77-a68c-810ded18670c
keywords:
- Windows SDK de formato multimedia, uso compartido de ancho de banda
- Formato de sistemas avanzados (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- uso compartido de ancho de banda, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2b9ea05210e39c54334373be725284dbd1affc0170be6568600eeb4c2bead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055595"
---
# <a name="bandwidth-sharing-types"></a>Tipos de uso compartido de ancho de banda

Puede usar tipos de uso compartido de ancho de banda para identificar la naturaleza de un objeto de uso compartido de ancho de banda en un perfil. Los tipos de uso compartido de ancho de banda se usan como parámetros para [**IWMBandwidthSharing::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype) e [**IWMBandwidthSharing::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype).

En la tabla siguiente se enumeran los identificadores de los tipos de uso compartido de ancho de banda.



| Constante de tipo de uso compartido de ancho de banda      | GUID                                 |
|--------------------------------------|--------------------------------------|
| CLSID \_ WMBandwidthSharing \_ Exclusive | af6060aa-5197-11d2-b6af-00c04fd908e9 |
| CLSID \_ WMBandwidthSharing \_ Partial   | af6060ab-5197-11d2-b6af-00c04fd908e9 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Valores GUID**](guid-values.md)
</dt> </dl>

 

 




