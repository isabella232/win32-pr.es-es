---
title: Propiedad de dominio IMsTscAx
description: Especifica el dominio en el que el usuario actual inicia sesión.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Propiedades de dominio Servicios de Escritorio remoto
- Propiedad de Servicios de Escritorio remoto , interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad Domain
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad Domain
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498098b57ef5ecb19958f6ef0e082022a92f15bab7f1fbfc74bef62d928e8726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125435"
---
# <a name="imstscaxdomain-property"></a>Propiedad IMsTscAx::D omain

Especifica el dominio en el que el usuario actual inicia sesión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>Valor de propiedad

Nuevo nombre de dominio.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Establecer la **propiedad Domain** es opcional. Si no está establecido, el usuario puede elegir un dominio cuando aparezca Windows cuadro de diálogo Inicio de sesión durante la conexión.

El **método get \_ Domain** asigna la memoria necesaria para el búfer al que apunta el *parámetro pDomain.* La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la [**función SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Esto no es necesario para Visual Basic y clientes de scripting.

Esta propiedad solo se puede establecer si el control no está en el estado conectado. Devuelve **E \_ FAIL si** se llama cuando se conecta el control. Puede comprobar si el control está conectado respondiendo a eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md) o examinando la [**propiedad Connected.**](imstscax-connected.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsTscAx se define como \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**Conectado**](imstscax-connected.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

