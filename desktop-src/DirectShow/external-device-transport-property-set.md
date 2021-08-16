---
description: Conjunto de propiedades de transporte de dispositivos externos
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propiedades de transporte de dispositivos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef7db31dfe80fae0178aa329ce7e3c6cd55d3a6acbef7fd5a8ccda07943bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685675"
---
# <a name="external-device-transport-property-set"></a>Conjunto de propiedades de transporte de dispositivos externos

Este conjunto de propiedades controla el transporte de datos hacia y desde un dispositivo externo. En la mayoría de los casos, las aplicaciones no deben usar este conjunto de propiedades directamente. En su [**lugar, use la interfaz IAMExtTransport.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

En la tabla siguiente se enumeran las propiedades que son relevantes para las aplicaciones en modo de usuario. Para obtener una descripción completa de este conjunto de propiedades, consulte el DDK de Microsoft Windows Driver Development Kit.



| Etiqueta | Valor |
|-------------------|---------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_ |



 



| Id. de propiedad                                                                           | Descripción                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Busca un número de seguimiento absoluto (ATN). |
| [**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**](ksproperty-extxport-timecode-search.md) | Busca un código de hora.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



