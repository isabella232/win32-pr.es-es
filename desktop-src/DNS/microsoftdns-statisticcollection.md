---
title: MicrosoftDNS_StatisticCollection
description: La clase StatisticCollection de MicrosoftDNS \_ representa una colección de estadísticas relacionadas del servidor DNS.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109097"
---
# <a name="microsoftdns_statisticcollection"></a>StatisticCollection de MicrosoftDNS \_

La clase StatisticCollection de MicrosoftDNS \_ representa una colección de estadísticas relacionadas del servidor DNS.

La sintaxis siguiente se simplifica a partir del código MOF.

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>Propiedades

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**
</dt> <dd>

Nombre de la colección de estadísticas.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

Representación numérica de la colección de estadísticas.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Estadísticas de \_ MicrosoftDNS\[\]**
</dt> <dd>

Matriz de valores asociados a la estadística.

</dd> </dl>

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Esta clase no tiene métodos.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Estadística de \_ MicrosoftDNS**](microsoftdns-statistic.md)
</dt> </dl>

 

 




