---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720294"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_

Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .

Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Salida**
</dt> <dd>

Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.

</dd> <dt>

**BusType**
</dt> <dd>

Una operación **OR bit a bit** de marcas de la enumeración [**D3DBUSTYPE**](d3dbustype.md) .

</dd> <dt>

**bAccessibleInContiguousBlocks**
</dt> <dd>

Si **es true**, los bloques contiguos de memoria de vídeo pueden estar accesibles para la CPU o el bus.

</dd> <dt>

**bAccessibleInNonContiguousBlocks**
</dt> <dd>

Si **es true**, los bloques no contiguos de memoria de vídeo pueden estar accesibles para la CPU o el bus.

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

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




