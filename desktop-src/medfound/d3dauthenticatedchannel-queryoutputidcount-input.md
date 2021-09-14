---
description: Contiene datos de entrada para una consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361160"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ INPUT structure

Contiene datos de entrada para una [**consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.**](d3dauthenticatedquery-outputidcount.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Entrada**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT**](d3dauthenticatedchannel-query-input.md) que contiene el GUID de la consulta y otros datos.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Identificador del dispositivo.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Identificador de la sesión criptográfica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




