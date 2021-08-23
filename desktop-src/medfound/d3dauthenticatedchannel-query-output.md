---
description: Contiene la respuesta del método IDirect3DAuthenticatedChannel9::Query.
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2defeaf134db9a2464854554db721586f592fc62110d172e0ac804e010804966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600835"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT structure

Contiene la respuesta del [**método IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Omac**
</dt> <dd>

Estructura [**\_ OMAC D3D**](d3d-omac.md) que contiene un código de autenticación de mensajes (MAC) de los datos. El controlador usa mac CBC (OMAC) basado en AES basado en una clave para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**Querytype**
</dt> <dd>

GUID que especifica la consulta. Para obtener una lista de valores, [vea Content Protection Queries](content-protection-queries.md).

</dd> <dt>

**Manejar**
</dt> <dd>

Identificador del canal autenticado.

</dd> <dt>

**UINT**
</dt> <dd>

Número de secuencia de consulta.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Código de resultado de la consulta.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para los **miembros QueryType,** **hChannel** y **SequenceNumber,** el controlador usa en los mismos valores que la aplicación proporcionó en la estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT.**](d3dauthenticatedchannel-query-input.md) La aplicación debe comprobar que estos valores coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




