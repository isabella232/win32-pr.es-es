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
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468768"
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



## <a name="members"></a>Members

<dl> <dt>

**Omac**
</dt> <dd>

Estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autenticación de mensajes (MAC) de los datos. El controlador usa mac CBC (OMAC) de una clave basado en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**Querytype**
</dt> <dd>

GUID que especifica la consulta. Para obtener una lista de valores, [vea Content Protection Queries](content-protection-queries.md).

</dd> <dt>

**MANEJAR**
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

## <a name="remarks"></a>Observaciones

Para los **miembros QueryType,** **hChannel** y **SequenceNumber,** el controlador usa en los mismos valores que la aplicación proporcionada en la estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ INPUT.**](d3dauthenticatedchannel-query-input.md) La aplicación debe comprobar que estos valores coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




