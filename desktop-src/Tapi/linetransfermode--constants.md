---
description: Las constantes de marca de bits LINETRANSFERMODE \_ describen distintas formas de resolver solicitudes de transferencia de llamadas.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: LINETRANSFERMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374779"
---
# <a name="linetransfermode_-constants"></a>Constantes \_ LINETRANSFERMODE

Las constantes de marca de bits **LINETRANSFERMODE \_** describen distintas formas de resolver solicitudes de transferencia de llamadas.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE \_ CONFERENCE**
</dt> <dd> <dl> <dt>



La transferencia se resuelve estableciendo una conferencia triple entre la aplicación, la parte conectada a la llamada inicial y la parte conectada a la llamada de consulta. Cuando se selecciona esta opción, se crea una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE \_ TRANSFER**
</dt> <dd> <dl> <dt>



La transferencia se resuelve transfiriendo la llamada inicial a la llamada de consulta. Ambas llamadas pasarán a estar inactivas en la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




