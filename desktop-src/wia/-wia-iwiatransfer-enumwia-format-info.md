---
description: Crea un enumerador para los formatos de transferencia que admite el Windows Image Acquisition (WIA) 2.0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: Método IWiaTransfer::EnumWIA_FORMAT_INFO (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362803"
---
# <a name="iwiatransferenumwia_format_info-method"></a>IWiaTransfer::EnumWIA \_ FORMAT \_ INFO (método)

Crea un enumerador para los formatos de transferencia que admite el Windows Image Acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Dirección del puntero a la interfaz [**IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para el enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) el puntero de interfaz recibido a través del parámetro *ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
