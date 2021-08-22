---
description: Contiene datos de entrada para un comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742911"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE (estructura)

Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.**](d3dauthenticatedconfigure-sharedresource.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Parámetros**
</dt> <dd>

Estructura [**INPUT de D3DAUTHENTICATEDCHANNEL \_ QUE \_**](d3dauthenticatedchannel-configure-input.md) contiene el GUID del comando y otros datos.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Valor [**\_ PROCESSIDENTIFIERTYPE de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-processidentifiertype.md) que especifica el tipo de proceso. Para especificar el Administrador de ventanas de escritorio (DWM), establezca este miembro en **PROCESSIDTYPE \_ DWM**. De lo contrario, establezca este miembro en **PROCESSIDTYPE \_ HANDLE** y establezca el **miembro ProcessHandle** en un identificador válido.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Un identificador de proceso. Si el **miembro ProcessIdentifier** es igual a **PROCESSTIDTYPE \_ HANDLE**, el **miembro ProcessHandle** especifica un identificador para un proceso. De lo contrario, se omite el valor.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Si **es TRUE,** el proceso especificado tiene acceso a recursos compartidos restringidos.

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

 

 




