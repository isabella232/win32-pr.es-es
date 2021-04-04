---
title: Propiedad EnableSuperPan de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableSuperPan
- Propiedad EnableSuperPan Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableSuperPan
- Propiedad EnableSuperPan Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableSuperPan
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
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802750"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>IMsRdpClientAdvancedSettings7:: EnableSuperPan (propiedad)

Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado. SuperPan es una característica que permite a los usuarios navegar con facilidad por un escritorio remoto en modo de pantalla completa, cuando las dimensiones del escritorio remoto son mayores que las dimensiones de la ventana del cliente actual. En lugar de usar barras de desplazamiento para navegar por el escritorio, el usuario puede apuntar al borde de la ventana y el escritorio remoto se desplazará automáticamente en esa dirección. SuperPan no admite más de un monitor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Valor de propiedad

Un **valor \_ booleano Variant** que especifica si SuperPan está habilitado. Un valor de **Variant \_ true** especifica que SuperPan está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
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

 

 





