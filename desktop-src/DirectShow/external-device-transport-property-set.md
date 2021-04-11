---
description: Conjunto de propiedades de transporte de dispositivo externo
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propiedades de transporte de dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152696"
---
# <a name="external-device-transport-property-set"></a>Conjunto de propiedades de transporte de dispositivo externo

Este conjunto de propiedades controla el transporte de datos hacia y desde un dispositivo externo. En la mayoría de los casos, las aplicaciones no deben utilizar directamente esta propiedad establecida. En su lugar, use la interfaz [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .

En la tabla siguiente se enumeran las propiedades que son relevantes para las aplicaciones de modo de usuario. Para obtener una descripción completa de este conjunto de propiedades, consulte el DDK del kit de desarrollo de controladores de Microsoft Windows.



|                   |                           |
|-------------------|---------------------------|
| GUID del conjunto de propiedades | \_transporte ext \_ PROPSETID |



 



| Id. de propiedad                                                                           | Descripción                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_**](ksproperty-extxport-atn-search.md)           | Busca un número de pista absoluta (ATN). |
| [**KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_**](ksproperty-extxport-timecode-search.md) | Busca un código de hora.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



