---
description: Las \_ constantes de marcador de bits LINESPECIALINFO describen las señales de información especial que la red puede usar para notificar diversas operaciones de informes y de observación de la red.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes de LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679405"
---
# <a name="linespecialinfo_-constants"></a>Constantes de LINESPECIALINFO \_

Las constantes de marcador de bits **LINESPECIALINFO \_** describen las señales de información especial que la red puede usar para notificar diversas operaciones de informes y de observación de la red. Se trata de secuencias de tono codificadas especiales que se transmiten al principio de los anuncios grabados de aviso de red.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un número libre, AIS, un cambio de número de Centrex y una estación de no trabajo, código de acceso no marcado o marcado como mensaje de operador de interceptación manual (categoría de irregularidades del cliente). LINESPECIALINFO \_ CUSTIRREG también se muestra cuando se rechaza la información de facturación y cuando la dirección marcada se bloquea en el conmutador.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuito**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un circuito no o un anuncio de emergencia (categoría bloqueo de tronco).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**reordenación de LINESPECIALINFO \_**
</dt> <dd> <dl> <dt>



Este tono de información especial precede a un anuncio de reordenación (categoría de irregularidad del equipo). \_También se muestra el reorden de LINESPECIALINFO cuando el teléfono se mantiene OffHook demasiado largo.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO no \_ disponible**
</dt> <dd> <dl> <dt>



Los detalles sobre el tono de información especial no están disponibles y no serán conocidos.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ desconocido**
</dt> <dd> <dl> <dt>



Actualmente, se desconocen los detalles del tono de información especial, pero se pueden conocer más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Los tonos de información especiales se definen para los mensajes de consulta y no se utilizan normalmente para fines de facturación o de supervisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




