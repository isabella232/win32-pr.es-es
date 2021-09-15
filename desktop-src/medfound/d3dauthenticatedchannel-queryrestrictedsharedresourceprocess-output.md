---
description: Contiene la respuesta a una consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468761"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT structure

Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS.**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Salida**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) que contiene un código de autenticación de mensajes (MAC) y otros datos.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

Índice del proceso en la lista de procesos.

</dd> <dt>

**ProcessIdentifer**
</dt> <dd>

Valor [**\_ PROCESSIDENTIFIERTYPE de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-processidentifiertype.md) que especifica el tipo de proceso.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Un identificador de proceso. Si el **miembro ProcessIdentifier** es igual a **PROCESSIDTYPE \_ HANDLE**, el **miembro ProcessHandle** contiene un identificador válido para un proceso. De lo contrario, se omite este miembro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El Administrador de ventanas de escritorio (DWM) se identifica estableciendo **ProcessIdentifier** igual a **PROCESSIDTYPE \_ DWM.** Otros procesos se identifican estableciendo el identificador de proceso **en ProcessHandle** y estableciendo **ProcessIdentifier** igual a **PROCESSIDTYPE \_ HANDLE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




