---
description: Contiene datos de entrada para una \_ consulta de D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT estructura (D3d9types. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153653"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ \_ estructura de entrada QUERYOUTPUTIDCOUNT

Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Entrada**
</dt> <dd>

Una estructura de [**\_ \_ entrada de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) que contiene el GUID para la consulta y otros datos.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




