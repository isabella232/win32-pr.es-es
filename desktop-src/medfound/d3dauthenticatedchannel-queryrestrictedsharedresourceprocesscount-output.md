---
description: Contiene la respuesta a una consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT estructura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468760"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ OUTPUT structure

Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Salida**
</dt> <dd>

Estructura [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT**](d3dauthenticatedchannel-query-output.md) que contiene un código de autenticación de mensajes (MAC) y otros datos.

</dd> <dt>

**NumRestrictedSharedResourceProcesses**
</dt> <dd>

Número de procesos permitidos para abrir recursos compartidos con acceso restringido. Un proceso no puede abrir este tipo de recurso a menos que se le haya concedido acceso al proceso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




