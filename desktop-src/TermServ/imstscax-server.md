---
title: Propiedad del servidor IMsTscAx (Asptlb. h)
description: Especifica el nombre del servidor al que está conectado el control actual.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedades de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, propiedad de servidor
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996013"
---
# <a name="imstscaxserver-property"></a>IMsTscAx:: Server (propiedad)

Especifica el nombre del servidor al que está conectado el control actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del nuevo servidor. Este parámetro puede ser un nombre DNS o una dirección IP.

## <a name="error-codes"></a>Códigos de error

Si los métodos se realizan correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Esta propiedad debe establecerse antes de llamar al método [**Connect**](imstscax-connect.md) . Es la única propiedad que se debe establecer antes de la conexión.

Esta propiedad solo se puede establecer si el control no está en estado conectado. Esta propiedad devuelve **E \_ produce un error** si se llama cuando el control está conectado. Puede comprobar el estado conectado mediante la propiedad [**conectado**](imstscax-connected.md) .

Este método asigna la memoria necesaria para el búfer señalado por el parámetro *pServer* . La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Esto no es necesario para los clientes de scripting y Visual Basic.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Asptlb. h</dt> </dl>    |
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

 

