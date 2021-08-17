---
title: Propiedad IMsRdpClient4 AdvancedSettings5
description: Recupera un puntero a una interfaz IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto propiedad , AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto propiedad , AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto propiedad , AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto propiedad , AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto propiedad , AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto propiedad , AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb8efd8fae25be768a1b758389b5ca7c20a9f3f8b414e62acb865fecf83eeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138958"
---
# <a name="imsrdpclient4advancedsettings5-property"></a>Propiedad IMsRdpClient4::AdvancedSettings5

Recupera un puntero a una [**interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a la [**interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md) La interfaz se puede usar para establecer la configuración avanzada para el control de cliente.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Comentarios

Esta propiedad no se puede establecer cuando el control está conectado.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient4 se define como 095E0738-D97D-488b-B9F6-DD0E8D66C0DE<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





