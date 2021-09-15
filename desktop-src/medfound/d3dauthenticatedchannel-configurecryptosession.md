---
description: Contiene datos de entrada para un comando D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360467"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION (estructura)

Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION.**](d3dauthenticatedconfigure-cryptosession.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a>Members

<dl> <dt>

**Parámetros**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md) que contiene el GUID del comando y otros datos.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Identificador del dispositivo descodificador DirectX Video Acceleration 2 (DXVA-2).

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Identificador de la sesión criptográfica.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Identificador del dispositivo Direct3D.

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

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




