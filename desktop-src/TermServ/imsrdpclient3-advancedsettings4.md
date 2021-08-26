---
title: Propiedad IMsRdpClient3 AdvancedSettings4
description: Recupera un puntero a la interfaz IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto propiedad , AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto propiedad , AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e8bd4d5562f5f7b73eac6c580fe7b033a10b8ce7f0471b2d1ca969cd7ae0ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033545"
---
# <a name="imsrdpclient3advancedsettings4-property"></a>Propiedad IMsRdpClient3::AdvancedSettings4

Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a la [**interfaz IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md) La interfaz se puede usar para establecer la configuración avanzada para el control de cliente.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Comentarios

Esta propiedad no se puede establecer cuando el control está conectado.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClient3 se define como \_ 91b7cbc5-a72e-4fa0-9300-d647d7e897ff<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





