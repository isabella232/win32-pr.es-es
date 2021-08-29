---
description: Contiene datos de entrada para un comando D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 27f94dd5aca19d24742d553a65ce3c7f9164edf48cb1aab335d87d338f7e7499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958775"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE (estructura)

Contiene datos de entrada para un [**comando D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE.**](d3dauthenticatedconfigure-initialize.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Parámetros**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) que contiene el GUID del comando y otros datos.

</dd> <dt>

**StartSequenceQuery**
</dt> <dd>

Número de secuencia inicial de las consultas.

</dd> <dt>

**StartSequenceConfigure**
</dt> <dd>

Número de secuencia inicial de los comandos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los **miembros StartSequenceQuery** y **StartSequenceConfigure** contienen un número aleatorio de 32 bits seguro criptográficamente.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




