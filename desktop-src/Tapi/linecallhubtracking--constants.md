---
description: Las \_ constantes de marcador de bits LINECALLHUBTRACKING describen el tipo de seguimiento de centro de llamadas proporcionado.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes de LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679549"
---
# <a name="linecallhubtracking_-constants"></a>Constantes de LINECALLHUBTRACKING \_

Las constantes de marcador de bits **LINECALLHUBTRACKING \_** describen el tipo de seguimiento de centro de llamadas proporcionado.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**
</dt> <dd> <dl> <dt>



El seguimiento del centro de llamadas se proporciona en el nivel de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ ninguno**
</dt> <dd> <dl> <dt>



No se proporciona seguimiento del centro de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**
</dt> <dd> <dl> <dt>



Se realiza un seguimiento de los centros de llamadas en el nivel de proveedor de servicios. No se informan los cambios de llamada por llamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Cuando se producen cambios en esta estructura de datos, se envía un mensaje de [**línea \_ CALLINFO**](line-callinfo.md) a la aplicación. Los parámetros de este mensaje son un identificador de la llamada y una indicación del elemento de información que ha cambiado. La estructura de datos [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica qué tipo de seguimiento se proporciona.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ CALLINFO**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




