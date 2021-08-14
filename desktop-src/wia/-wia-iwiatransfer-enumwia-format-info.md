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
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669481"
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

## <a name="remarks"></a>Comentarios

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz recibido a través del *parámetro ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
