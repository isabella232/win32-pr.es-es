---
description: Contiene datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE estructura (D3d9types. h)
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
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696158"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGURESHAREDRESOURCE

Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

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

[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Un valor de [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) que especifica el tipo de proceso. Para especificar el proceso de Administrador de ventanas de escritorio (DWM), establezca este miembro en **PROCESSIDTYPE \_ DWM**. De lo contrario, establezca este miembro en **PROCESSIDTYPE \_ Handle** y establezca el miembro **ProcessHandle** en un identificador válido.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Identificador de proceso. Si el miembro **ProcessIdentifier** es igual **al \_ identificador PROCESSTIDTYPE**, el miembro **ProcessHandle** especifica un identificador para un proceso. De lo contrario, se omite el valor.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Si **es true**, el proceso especificado tiene acceso a recursos compartidos restringidos.

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

 

 




