---
description: Las constantes de marca de bits LINEBUSYMODE \_ describen las distintas señales ocupadas que el conmutador o la red pueden generar. Estas señales ocupadas normalmente indican que un recurso diferente que es necesario para realizar una llamada está actualmente en uso.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: LINEBUSYMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54563567944a2e5164717f7d64ff7026a0045ea735405a7bcad159969f07514a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681995"
---
# <a name="linebusymode_-constants"></a>Constantes LINEBUSYMODE \_

Las constantes de marca de bits **LINEBUSYMODE \_** describen las distintas señales ocupadas que el conmutador o la red pueden generar. Estas señales ocupadas normalmente indican que un recurso diferente que es necesario para realizar una llamada está actualmente en uso.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE \_ STATION**
</dt> <dd> <dl> <dt>



La señal de ocupado indica que la estación de la entidad a la que se llamó está ocupada. Normalmente, esto se señala con un *tono ocupado* normal.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**TRONCO LINEBUSYMODE \_**
</dt> <dd> <dl> <dt>



La señal ocupada indica que un tronco o circuito está ocupado. Normalmente, esto se señala con un *tono ocupado* rápido.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



El modo específico de la señal ocupada es desconocido actualmente, pero puede que se conozca más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



El modo específico de la señal ocupada no está disponible y no se conocerá.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

> [!Note]  
> Las señales ocupadas se pueden enviar como tonos de banda o mensajes fuera de banda. TAPI no hace ninguna suposición sobre el mecanismo de señalización específico.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




