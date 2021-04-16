---
description: Crea un enumerador para los formatos de transferencia que admite el dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer:: EnumWIA_FORMAT_INFO (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686830"
---
# <a name="iwiatransferenumwia_format_info-method"></a>Método de información de \_ formato IWiaTransfer:: EnumWIA \_

Crea un enumerador para los formatos de transferencia que admite el dispositivo de adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIEnum* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ \_ información de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Dirección del puntero a la interfaz de [**\_ \_ información de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para el enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz recibido a través del parámetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
