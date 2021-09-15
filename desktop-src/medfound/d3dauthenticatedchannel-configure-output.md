---
description: Contiene la respuesta a una llamada al método IDirect3DAuthenticatedChannel9::Configure.
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572860"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ OUTPUT structure

Contiene la respuesta a una llamada al [**método IDirect3DAuthenticatedChannel9::Configure.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Omac**
</dt> <dd>

Estructura [**\_ OMAC D3D**](d3d-omac.md) que contiene un código de autenticación de mensajes (MAC) de los datos. El controlador usa mac CBC de una clave (OMAC) basado en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID que especifica el comando. Para obtener una lista de valores, [vea Content Protection Comandos](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Identificador del canal autenticado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Número de secuencia del comando.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Código de resultado del comando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para los **miembros ConfigureType,** **hChannel** y **SequenceNumber,** el controlador usa los mismos valores que la aplicación proporcionó en la estructura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT.**](d3dauthenticatedchannel-configure-input.md) La aplicación debe comprobar que estos valores coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




