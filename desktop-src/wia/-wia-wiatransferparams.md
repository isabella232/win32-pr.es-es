---
description: 'El WiaTransferParams se transmite a una aplicación durante una transferencia de datos mediante el sistema de tiempo de ejecución de adquisición de imágenes de Windows (WIA) al método IWiaTransferCallback:: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estructura WiaTransferParams (WIA. h)
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
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696494"
---
# <a name="wiatransferparams-structure"></a>Estructura WiaTransferParams

El **WiaTransferParams** se transmite a una aplicación durante una transferencia de datos mediante el sistema de tiempo de ejecución de adquisición de imágenes de Windows (WIA) al método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .

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

Tipo: **Long**

</dd> <dd>

Indica el estado de la transferencia de datos.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_Estado de \_ mensaje de transferencia de WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ final \_ de la secuencia del mensaje de transferencia de \_ WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fin \_ de la transferencia del mensaje de transferencia de \_ WIA**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_Estado del \_ dispositivo de mensajes de transferencia WIA \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ Página nuevo mensaje de transferencia de WIA \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Indica el progreso de la transferencia de datos como un porcentaje.

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

El estado, o estado de error, del dispositivo establecido por el controlador; por ejemplo, "preparando".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




