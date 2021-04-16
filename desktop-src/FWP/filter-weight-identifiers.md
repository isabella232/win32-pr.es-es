---
title: Identificadores de peso de filtro (Fwpmu. h)
description: Filtrar los identificadores de peso utilizados por el motor de filtrado de base (BFE) para calcular los pesos de los filtros generados automáticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686150"
---
# <a name="filter-weight-identifiers"></a>Identificadores de peso de filtro

A continuación se enumeran los identificadores de peso de filtro utilizados por el motor de filtrado de base (BFE) para calcular los pesos de los filtros generados automáticamente.

Vea [filtrar asignación de peso](filter-weight-assignment.md) para obtener más información sobre la generación de pesos del filtro.

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM \_ \_ bits de ponderación automática \_**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Número de bits usados para pesos de filtro generados automáticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ de \_ peso automático \_ máximo**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Peso máximo de filtro generado automáticamente.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**
</dt> <dd> <dl> <dt>

0XC
</dt> <dt>



BFE asigna un peso con este valor de intervalo a los filtros IKE y AuthIP.

Consulte [exenciones de IKE/AuthIP](ike-exemptions.md) para obtener más información sobre los filtros IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**intervalo de peso de FWPM de \_ \_ \_ IPSec**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE asigna un peso con este valor de intervalo a los filtros de la Directiva de IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_ \_ rango máximo de peso de FWPM \_**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Valor máximo permitido para el intervalo de peso del filtro.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** representa el mayor valor posible de **UINT64**. El valor de esta constante es 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





