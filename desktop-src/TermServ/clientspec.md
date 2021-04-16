---
title: Enumeración ClientSpec
description: Se usa con la propiedad ClientProtocolSpec para especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ClientSpec
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
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676614"
---
# <a name="clientspec-enumeration"></a>Enumeración ClientSpec

Se usa con la propiedad [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) para especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.

## <a name="syntax"></a>Sintaxis


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

El protocolo es el protocolo de Escritorio remoto de Windows 8 completo.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**
</dt> <dd>

El protocolo se limita al uso del códec de Windows 7 con SP1 RemoteFX y una caché más pequeña. El resto de los códecs están deshabilitados. Este protocolo tiene la superficie de memoria más pequeña.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**
</dt> <dd>

El protocolo es el mismo que **FullMode**, salvo que usa una caché más pequeña.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





