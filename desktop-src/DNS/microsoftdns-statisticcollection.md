---
title: MicrosoftDNS_StatisticCollection
description: La \_ clase MicrosoftDNS StatisticCollection representa una colección de estadísticas relacionadas del servidor DNS.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f9c65714fb3b1db58b5a6439ade5531792501
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075479"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ StatisticCollection

La \_ clase MicrosoftDNS StatisticCollection representa una colección de estadísticas relacionadas del servidor DNS.

La siguiente sintaxis se simplifica desde el código MOF.

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

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**
</dt> <dd>

Nombre de la colección de estadísticas.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

Representación numérica de la colección de estadísticas.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Estadísticas de estadísticas de MicrosoftDNS \_\[\]**
</dt> <dd>

Matriz de valores asociados a la estadística.

</dd> </dl>

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Esta clase no tiene métodos.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Estadística de MicrosoftDNS \_**](microsoftdns-statistic.md)
</dt> </dl>

 

 




