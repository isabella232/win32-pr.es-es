---
title: Enumeración ClientSpec
description: Se usa con la propiedad ClientProtocolSpec para especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Enumeración ClientSpec Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5706600ea0854a3b83d961965ba3cc8f0084c2969fc31438344378781410729f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856387"
---
# <a name="clientspec-enumeration"></a>Enumeración ClientSpec

Se usa con [**la propiedad ClientProtocolSpec para**](imsrdpclientadvancedsettings8-clientprotocolspec.md) especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**
</dt> <dd>

El protocolo es completo Windows 8 Escritorio remoto protocolo.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**
</dt> <dd>

El protocolo se limita al uso de la Windows 7 con el códec de RemoteFX SP1 y una memoria caché más pequeña. Todos los demás códecs están deshabilitados. Este protocolo tiene la superficie de memoria más pequeña.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**
</dt> <dd>

El protocolo es el mismo que **FullMode**, salvo que usa una memoria caché más pequeña.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





