---
title: Propiedad IMsTscAx DesktopWidth
description: Especifica el ancho del control actual, en píxeles, en el escritorio remoto inicial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Propiedad DesktopWidth Servicios de Escritorio remoto
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca982303208bb2badecf210c9590f627a7b3b57c5acd9ecd7f8fee0bbb70ec93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058853"
---
# <a name="imstscaxdesktopwidth-property"></a>Propiedad IMsTscAx::D esktopWidth

Especifica el ancho del control actual, en píxeles, en el escritorio remoto inicial.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Nuevo ancho, en píxeles.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

El establecimiento **de la propiedad DesktopWidth** es opcional, pero debe establecerse antes de llamar al [**Conectar**](imstscax-connect.md) método . Si no se especifica un ancho de escritorio o se establece en cero, el ancho del escritorio se establece en el ancho del control. Los valores mínimo y máximo dependen de la versión del sistema operativo del Escritorio remoto cliente.

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

200 mínimo, 8192 como máximo

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

200 como mínimo, 2048 como máximo

</dd> <dt>

Windows Vista
</dt> <dd>

200 como mínimo, 1200 como máximo

</dd> </dl>

Una vez establecida una conexión, los cambios en el ancho del control no cambian el ancho del escritorio remoto. En su lugar, el control muestra barras de desplazamiento o centra el escritorio remoto, según corresponda. Para cambiar el tamaño de escritorio de una conexión activa, use el [**método IMsRdpClient8::Reconnect.**](imsrdpclient8-reconnect.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





