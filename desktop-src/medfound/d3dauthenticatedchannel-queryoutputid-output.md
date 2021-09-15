---
description: Contiene la respuesta a una consulta OUTPUTID D3DAUTHENTICATEDQUERY. \_
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580008"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_ OUTPUT structure

Contiene la respuesta a una [**consulta \_ OUTPUTID D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-outputid.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**SALIDA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) que contiene un código de autenticación de mensajes (MAC) y otros datos.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Identificador del dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Identificador de la sesión criptográfica.

</dd> <dt>

**OutputIDIndex**
</dt> <dd>

Índice del identificador de salida especificado en el **miembro OutputID.**

</dd> <dt>

**OutputID**
</dt> <dd>

Identificador de salida asociado al dispositivo y la sesión criptográfica especificados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




