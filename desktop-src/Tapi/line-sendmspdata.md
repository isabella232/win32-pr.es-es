---
description: El mensaje SENDMSPDATA de la línea de TSPI \_ se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Mensaje de LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690225"
---
# <a name="line_sendmspdata-message"></a>Mensaje de línea \_ SENDMSPDATA

El mensaje **\_ SENDMSPDATA** de la línea de TSPI se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia (MSP).


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador de TAPI de la línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador de TAPI de la llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La línea de valor \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifica el MSP que debe recibir el mensaje. Si es 0, el mensaje se enviará a todos los MSP. Este es el identificador que se pasa a la [**función \_ LineCreateMSPInstance de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .

</dd> <dt>

*dwParam2* 
</dt> <dd>

Búfer que se va a pasar al MSP. TAPI no interpreta el búfer.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Tamaño, en bytes, del búfer en *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor de servicios debe negociar una versión de TAPI 3,0 o posterior para que este mensaje funcione.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca del proveedor de servicios multimedia (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

