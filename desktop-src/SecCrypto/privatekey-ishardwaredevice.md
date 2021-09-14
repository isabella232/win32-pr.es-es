---
description: Devuelve un valor booleano que indica si la clave privada se almacena en un dispositivo de hardware.
ms.assetid: 9a06f598-55cd-441b-a85f-8bec299f8245
title: Método PrivateKey.IsHardwareDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsHardwareDevice
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23b6fd379fd3a3b53fe0600dbf28481cd5ef2f86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170937"
---
# <a name="privatekeyishardwaredevice-method"></a>Método PrivateKey.IsHardwareDevice

\[El **método IsHardwareDevice** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método IsHardwareDevice** devuelve un valor booleano que indica si la clave privada se almacena en un dispositivo de hardware.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.IsHardwareDevice()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si es true, la clave privada se almacena en un dispositivo de hardware.

## <a name="remarks"></a>Observaciones

El valor devuelto de este método depende del proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado. Este método devolverá un valor de confianza si se usa un CSP de Microsoft. Si el CSP no es un CSP de Microsoft, no se puede confiar en que el valor devuelto sea preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
