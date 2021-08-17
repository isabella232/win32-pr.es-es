---
title: Propiedad IMsRdpClientAdvancedSettings3 ConnectionBarShowMinimizeButton
description: Especifica si se debe mostrar el botón Minimizar en la barra de conexión.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f1ef263868d29685242962e4538bd84635138fb0f205194d8c27c5b6932aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058963"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a>Propiedad IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton

Especifica si se debe mostrar el **botón Minimizar** en la barra de conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **VARIANT \_ TRUE para** mostrar el botón **Minimizar** y en **VARIANT \_ FALSE** para deshabilitar la presentación del **botón Minimizar.**

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Esta propiedad no se puede establecer mientras el control está conectado.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 se define como 19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





