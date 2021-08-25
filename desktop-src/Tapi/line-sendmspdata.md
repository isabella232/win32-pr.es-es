---
description: El mensaje TSPI LINE SENDMSPDATA se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia \_ (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: LINE_SENDMSPDATA mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90a4f9086bb734f73a9a28817009c11d261442cf4253791b51e48e89d511b2ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126215"
---
# <a name="line_sendmspdata-message"></a>Mensaje \_ LINE SENDMSPDATA

El mensaje TSPI **LINE \_ SENDMSPDATA** se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia (MSP).


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador TAPI de la línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador tapi de la llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valor LINE \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifica el MSP que debe recibir el mensaje. Si es 0, el mensaje se enviará a todos los MSP. Este es el identificador que se pasa a la [**función \_ LineCreateMSPInstance de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Búfer que se pasará al MSP. TAPI no interpreta el búfer.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Tamaño, en bytes, del búfer en *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El proveedor de servicios debe negociar una versión 3.0 o posterior de TAPI para que este mensaje funcione.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca del proveedor de Media Service (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**Línea \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**Línea \_ TSPIRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

