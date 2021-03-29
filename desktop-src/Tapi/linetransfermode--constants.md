---
description: Las \_ constantes de marcador de bits LINETRANSFERMODE describen diferentes maneras de resolver las solicitudes de transferencia de llamadas.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes de LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679061"
---
# <a name="linetransfermode_-constants"></a>Constantes de LINETRANSFERMODE \_

Las constantes de marcador de bits **LINETRANSFERMODE \_** describen diferentes maneras de resolver las solicitudes de transferencia de llamadas.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**Conferencia de LINETRANSFERMODE \_**
</dt> <dd> <dl> <dt>



La transferencia se resuelve mediante el establecimiento de una conferencia de tres vías entre la aplicación, la entidad conectada a la llamada inicial y la entidad conectada a la llamada de consulta. Cuando se selecciona esta opción, se crea una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**transferencia de LINETRANSFERMODE \_**
</dt> <dd> <dl> <dt>



La transferencia se resuelve transfiriendo la llamada inicial a la llamada de consulta. Ambas llamadas se volverán inactivas a la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




