---
description: Contiene los datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE estructura (D3d9types. h)
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
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080323"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a>D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGUREINITIALIZE

Contiene los datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

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

[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.

</dd> <dt>

**StartSequenceQuery**
</dt> <dd>

Número de secuencia inicial para las consultas.

</dd> <dt>

**StartSequenceConfigure**
</dt> <dd>

El número de secuencia inicial para los comandos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada uno de los miembros **StartSequenceQuery** y **StartSequenceConfigure** contiene un número aleatorio de 32 bits criptográficamente seguro.

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

[**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




