---
description: Conjunto de propiedades de transporte de dispositivos externos
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propiedades de transporte de dispositivos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255207"
---
# <a name="external-device-transport-property-set"></a>Conjunto de propiedades de transporte de dispositivos externos

Este conjunto de propiedades controla el transporte de datos hacia y desde un dispositivo externo. En la mayoría de los casos, las aplicaciones no deben usar directamente este conjunto de propiedades. Use la [**interfaz IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) en su lugar.

En la tabla siguiente se enumeran las propiedades que son relevantes para las aplicaciones en modo de usuario. Para obtener una descripción completa de este conjunto de propiedades, consulte el DDK Windows Driver Development Kit de Microsoft.



| Etiqueta | Value |
|-------------------|---------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_ |



 



| Id. de propiedad                                                                           | Descripción                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Busca un número de seguimiento absoluto (ATN). |
| [**BÚSQUEDA DE CÓDIGO \_ DE TIEMPO DE EXTXPORT \_ DE KSPROPERTY \_**](ksproperty-extxport-timecode-search.md) | Busca un código de hora.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



