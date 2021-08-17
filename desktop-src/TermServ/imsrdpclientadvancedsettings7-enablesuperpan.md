---
title: Propiedad EnableSuperPan de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Propiedad EnableSuperPan Servicios de Escritorio remoto
- Propiedad EnableSuperPan Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad EnableSuperPan
- Propiedad EnableSuperPan Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd48fbb42f65e42b0cdeee3560c93361c49283eecfa4ee3a792a19f6081b07b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757351"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>IMsRdpClientAdvancedSettings7::EnableSuperPan, propiedad

Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado. SuperPan es una característica que permite a un usuario navegar fácilmente por un escritorio remoto en modo de pantalla completa, cuando las dimensiones del escritorio remoto son mayores que las dimensiones de la ventana de cliente actual. En lugar de usar barras de desplazamiento para navegar por el escritorio, el usuario puede apuntar al borde de la ventana y el escritorio remoto se desplazará automáticamente en esa dirección. SuperPan no admite más de un monitor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Valor de propiedad

Valor **VARIANT \_ BOOL** que especifica si SuperPan está habilitado. El valor **VARIANT \_ TRUE** especifica que SuperPan está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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
</dt> </dl>

 

 





