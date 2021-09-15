---
description: Contiene datos de entrada para una consulta CRYPTOSESSION D3DAUTHENTICATEDQUERY. \_
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468765"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ INPUT structure

Contiene datos de entrada para una [**consulta \_ CRYPTOSESSION D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-cryptosession.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Entrada**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT**](d3dauthenticatedchannel-query-input.md) que contiene el GUID de la consulta y otros datos.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Identificador de un dispositivo descodificador de Aceleración de vídeo 2 (DXVA-2) de DirectX.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




