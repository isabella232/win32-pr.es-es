---
title: Propiedad KeyboardHookMode de IMsRdpClientSecuredSettings
description: Especifica la configuración de redirección de teclado, que especifica cómo y cuándo aplicar el método abreviado de teclado de Windows (por ejemplo, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad KeyboardHookMode
- Propiedad KeyboardHookMode Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422131"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>IMsRdpClientSecuredSettings:: KeyboardHookMode (propiedad)

Especifica la configuración de redirección de teclado, que especifica cómo y cuándo aplicar el método abreviado de teclado de Windows (por ejemplo, ALT + TAB).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Valor de propiedad

La nueva configuración. Este parámetro puede ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

Aplique las combinaciones de teclas solo localmente en el equipo cliente.

</dd> <dt>

1
</dt> <dd>

Aplique combinaciones de teclas en el servidor remoto.

</dd> <dt>

2
</dt> <dd>

Aplicar combinaciones de teclas al servidor remoto solo cuando el cliente se ejecuta en modo de pantalla completa. Este es el valor predeterminado.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Estas propiedades no se pueden establecer cuando el control está conectado.

Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





