---
description: Contiene datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION estructura (D3d9types. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696161"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a>D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGURECRYPTOSESSION

Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Parámetros**
</dt> <dd>

[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

Un identificador para el dispositivo descodificador DirectX video Acceleration 2 (DXVA-2).

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




