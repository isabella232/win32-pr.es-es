---
title: Propiedad AuthenticationType IMsRdpClientAdvancedSettings6
description: Especifica el tipo de autenticación utilizado para esta conexión.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Propiedad AuthenticationType Servicios de Escritorio remoto
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AuthenticationType
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AuthenticationType
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150289"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a>IMsRdpClientAdvancedSettings6:: AuthenticationType (propiedad)

Especifica el tipo de autenticación utilizado para esta conexión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe un valor que especifica el tipo de autenticación utilizado para esta conexión. Puede ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

No se usa autenticación.

</dd> <dt>

1
</dt> <dd>

Se usa la autenticación de certificado.

</dd> <dt>

2
</dt> <dd>

Se usa la autenticación Kerberos.

</dd> <dt>

3
</dt> <dd>

Se usan la autenticación de certificados y Kerberos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





