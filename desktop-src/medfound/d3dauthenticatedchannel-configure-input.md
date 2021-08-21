---
description: Contiene datos de entrada para el método IDirect3DAuthenticatedChannel9::Configure.
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: de968c83fee7ae68dcd756bdf83d529593eeb30b3c2776b03cda812bcd442c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974744"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT structure

Contiene datos de entrada [**para el método IDirect3DAuthenticatedChannel9::Configure.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Omac**
</dt> <dd>

Estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autenticación de mensajes (MAC) de los datos. El controlador usa mac CBC (OMAC) de una clave basado en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID que especifica el comando. Para obtener una lista de valores, [vea Content Protection Comandos](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Identificador del canal autenticado. Para obtener el identificador, llame a [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Número de secuencia de consulta. Al principio de la sesión, genere un número aleatorio de 32 bits seguro criptográficamente para usarlo como número de secuencia inicial. Para cada comando, incremente el número de secuencia en 1.

</dd> </dl>

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

 

 




