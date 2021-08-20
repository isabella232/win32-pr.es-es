---
description: Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo no actualizado.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumeración UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 3b0d2145f649cfdbd6c652213b95f0051a1d9d408d5ad4ef17a703c86b83781a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957673"
---
# <a name="updateimpactlevel-enumeration"></a>Enumeración UpdateImpactLevel

Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo no actualizado. Esta enumeración la usan normalmente las estructuras [**UpdateAssessment,**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) que a su vez están anidadas dentro del [**objeto OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) devuelto de [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Syntax


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Ninguno**
</dt> <dd>

No hay ningún impacto previsible en el dispositivo. Esto puede deberse a que el dispositivo está actualizado o no está actualizado porque el dispositivo está respetando sus períodos de aplazamiento de Windows Update for Business o está des actualizado, pero aún no ha alcanzado el umbral **daysOutOfDate** para alcanzar un nivel de impacto mayor.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ Low**
</dt> <dd>

El dispositivo no ejecuta el sistema operativo más reciente, pero tiene una actualización reciente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Medio**
</dt> <dd>

El dispositivo ejecuta el sistema operativo más reciente, pero tiene una actualización moderadamente reciente.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ High**
</dt> <dd>

El dispositivo ha estado fuera de fecha durante mucho tiempo. Este dispositivo puede tener vulnerabilidades de seguridad y puede que falte alguna corrección importante que Windows mejor. Cuando un dispositivo ejecuta una versión de Windows que ya no se admite, siempre se devuelve **UpdateImpactLevel \_ High.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando [**se llama a GetOSUpdateAssessment,**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) se devuelve una estructura [**OSUpdateAssessment.**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) Dentro de la estructura hay una **assessmentForCurrent** y **assessmentForUpToDate**. Ambos son estructuras [**UpdateAssessment.**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) Ambos miembros tienen una **enumeración UpdateImpactLevel,** que indica un impacto alto, medio, bajo o ningún impacto para un dispositivo que ejecuta un sistema operativo no actualizado. El valor de **daysOutOfDate** determina estos niveles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                   |
| Idl<br/>                      | <dl> <dt>WaaSAPI.idl</dt> </dl> |



 

 




