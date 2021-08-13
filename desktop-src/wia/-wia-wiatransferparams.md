---
description: WiaTransferParams se transmite a una aplicación durante una transferencia de datos por el sistema en tiempo de ejecución de adquisición de imágenes (WIA) de Windows al método IWiaTransferCallback::TransferCallback.
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estructura WiaTransferParams (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449915"
---
# <a name="wiatransferparams-structure"></a>Estructura WiaTransferParams

**WiaTransferParams** se transmite a una aplicación durante una transferencia de datos por el sistema en tiempo de ejecución de adquisición de imágenes (WIA) de Windows al método [**IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Miembros

<dl> <dt>

**lMessage**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica el estado de la transferencia de datos.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**ESTADO DE \_ MENSAJES DE \_ TRANSFERENCIA DE WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ STREAM**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA \_ TRANSFER \_ MSG \_ END \_ OF \_ TRANSFER**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**ESTADO DEL \_ DISPOSITIVO WIA TRANSFER \_ MSG \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**NUEVA \_ PÁGINA DE \_ MENSAJES DE TRANSFERENCIA \_ DE \_ WIA**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica el progreso de la transferencia de datos como porcentaje.

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

Tipo: **ULONG64**

</dd> <dd>

Indica la cantidad de datos transferidos.

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

El estado, o estado de error, del dispositivo establecido por el controlador; por ejemplo, "warming up".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




