---
title: Propiedad IMsTscAx AdvancedSettings
description: Recupera un puntero de interfaz IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Propiedad AdvancedSettings Servicios de Escritorio remoto
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fa39bd56c33d35b96cf98b1756e13e0de1796bff12ad3cc32f99a341068e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657295"
---
# <a name="imstscaxadvancedsettings-property"></a>Propiedad IMsTscAx::AdvancedSettings

Recupera un puntero [**de interfaz IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero [**de interfaz IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





