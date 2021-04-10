---
description: 'Contiene datos de entrada para el método IDirect3DAuthenticatedChannel9:: configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT estructura (D3d9types. h)
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
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275134"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurar la \_ estructura de entrada

Contiene datos de entrada para el método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

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

**omac**
</dt> <dd>

Una estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autentificación de mensajes (Mac) (Mac) de los datos. El controlador utiliza una clave CBC MAC (OMAC) basada en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID que especifica el comando. Para obtener una lista de valores, vea [comandos Content Protection](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Identificador del canal autenticado. Para obtener el identificador, llame a [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

El número de secuencia de la consulta. Al inicio de la sesión, genere un número aleatorio de 32 bits criptográficamente seguro para usarlo como el número de secuencia inicial. Para cada comando, incremente el número de secuencia en 1.

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

[**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




