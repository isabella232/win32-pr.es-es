---
title: Propiedad SuperPanAccelerationFactor de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica el factor de aceleración de SuperPan. El factor de aceleración superpan determina la rapidez con la que se desplazará la pantalla en el modo SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Propiedad SuperPanAccelerationFactor Servicios de Escritorio remoto
- Propiedad SuperPanAccelerationFactor Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto propiedad , SuperPanAccelerationFactor
- Propiedad SuperPanAccelerationFactor Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto propiedad , SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d948f5a39211b16166b7117a509f6e1204ef41c964f7b59e92d20309cc84ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941588"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor, propiedad

Especifica o recupera un valor que indica el factor de aceleración de SuperPan. El factor de aceleración superpan determina la rapidez con la que se desplazará la pantalla en el modo SuperPan. El factor de aceleración es el número de píxeles que la vista de pantalla se desplaza en una dirección determinada para cada píxel de movimiento del mouse por parte del cliente.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Valor de propiedad

Factor de aceleración de SuperPan que se establecerá. El factor de aceleración de SuperPan es el número de píxeles que se desplaza la vista de pantalla en una dirección determinada para cada píxel de movimiento del mouse.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre SuperPan, [**vea EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





