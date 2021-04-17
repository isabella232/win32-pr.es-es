---
description: Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo obsoleto.
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
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666633"
---
# <a name="updateimpactlevel-enumeration"></a>Enumeración UpdateImpactLevel

Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo obsoleto. Esta enumeración se usa generalmente en las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , que a su vez se anidan dentro del [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) devuelto desde [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Sintaxis


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

No hay ningún impacto previsible en el dispositivo. Esto puede deberse a que el dispositivo está actualizado o no está actualizado, ya que el dispositivo está respetando su Windows Update para los períodos de aplazamiento de la empresa, o no está actualizada, pero aún no ha alcanzado el umbral de **daysOutOfDate** para alcanzar un nivel de impacto superior.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ bajo**
</dt> <dd>

El dispositivo no está ejecutando el sistema operativo más reciente, pero tiene una actualización reciente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Medio**
</dt> <dd>

El dispositivo está ejecutando el sistema operativo más reciente, pero tiene una actualización moderada.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ alto**
</dt> <dd>

El dispositivo no está actualizado durante mucho tiempo. Es posible que este dispositivo tenga vulnerabilidades de seguridad y que falten correcciones importantes que hagan que Windows funcione mejor. Cuando un dispositivo está ejecutando una versión de Windows que ya no se admite, siempre se devuelve **UpdateImpactLevel \_ High** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se llama a [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) , se devuelve una estructura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) . Dentro de la estructura hay un **assessmentForCurrent** y un **assessmentForUpToDate**. Ambas son estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) . Ambos miembros tienen una enumeración **UpdateImpactLevel** , que indica un impacto alto, medio, bajo o no en un dispositivo que ejecuta un sistema operativo obsoleto. Estos niveles vienen determinados por el valor de **daysOutOfDate**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




