---
title: Propiedad IMsRdpClient ColorDepth
description: Profundidad de color (en bits por píxel) de la conexión del control.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Propiedad ColorDepth Servicios de Escritorio remoto
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient
- IMsRdpClient interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient2
- IMsRdpClient2 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient3
- IMsRdpClient3 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient4
- IMsRdpClient4 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient5
- IMsRdpClient5 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient6
- IMsRdpClient6 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient7
- IMsRdpClient7 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient8
- IMsRdpClient8 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient9
- IMsRdpClient9 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient10
- IMsRdpClient10 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151018"
---
# <a name="imsrdpclientcolordepth-property"></a>IMsRdpClient:: ColorDepth (propiedad)

Profundidad de color (en bits por píxel) de la conexión del control.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a>Valor de propiedad

Profundidad de color. Los valores son 8, 15, 16, 24 y 32 bits por píxel.

## <a name="error-codes"></a>Códigos de error

Si los métodos se realizan correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

No se puede establecer esta propiedad cuando el control está conectado.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





