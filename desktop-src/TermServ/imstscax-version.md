---
title: IMsTscAx Version, propiedad
description: Especifica el número de versión del control actual.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Propiedad Version Servicios de Escritorio remoto
- Propiedad version Servicios de Escritorio remoto , interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad Version
- Propiedad version Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8911eaaf8af95e0f3ca1fde254250bcc781e71450b7d96ce8dc342b36298d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770855"
---
# <a name="imstscaxversion-property"></a>Propiedad IMsTscAx::Version

Especifica el número de versión del control actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a>Valor de propiedad

El número de versión.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Este método asigna la memoria necesaria para el búfer al que apunta el *parámetro pVersion.* La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la [**función SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Esto no es necesario para los clientes Visual Basic y scripting.

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

 

