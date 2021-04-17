---
description: Las \_ constantes de marcador de bits LINEBUSYMODE describen diferentes señales de ocupación que el conmutador o la red pueden generar. Estas señales ocupadas suelen indicar que se está usando un recurso diferente necesario para realizar una llamada.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes de LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681090"
---
# <a name="linebusymode_-constants"></a>Constantes de LINEBUSYMODE \_

Las constantes de marcador de bits **LINEBUSYMODE \_** describen diferentes señales de ocupación que el conmutador o la red pueden generar. Estas señales ocupadas suelen indicar que se está usando un recurso diferente necesario para realizar una llamada.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_estación LINEBUSYMODE**
</dt> <dd> <dl> <dt>



La señal ocupado indica que la estación de la entidad a la que se ha llamado está ocupada. Normalmente, se señala con un tono ocupado *normal* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_tronco LINEBUSYMODE**
</dt> <dd> <dl> <dt>



La señal ocupado indica que un tronco o circuito está ocupado. Normalmente, se señala con un tono de uso *rápido* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ desconocido**
</dt> <dd> <dl> <dt>



Actualmente, el modo específico de la señal ocupado es desconocido, pero se puede conocer más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE no \_ disponible**
</dt> <dd> <dl> <dt>



El modo específico de la señal ocupado no está disponible y no se conocerá.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

> [!Note]  
> Las señales ocupadas se pueden enviar como tonos inbandes o mensajes fuera de banda. TAPI no realiza suposiciones sobre el mecanismo de señalización específico.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




