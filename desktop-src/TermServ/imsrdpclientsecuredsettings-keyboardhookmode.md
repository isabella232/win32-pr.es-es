---
title: IMsRdpClientSecuredSettings KeyboardHookMode, propiedad
description: Especifica la configuración de redireccionamiento del teclado, que especifica cómo y cuándo aplicar Windows método abreviado de teclado (por ejemplo, ALT+TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Propiedad KeyboardHookMode Servicios de Escritorio remoto
- Propiedad KeyboardHookMode Servicios de Escritorio remoto interfaz , IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto , propiedad KeyboardHookMode
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
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657595"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>IMsRdpClientSecuredSettings::KeyboardHookMode, propiedad

Especifica la configuración de redireccionamiento del teclado, que especifica cómo y cuándo aplicar Windows método abreviado de teclado (por ejemplo, ALT+TAB).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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

Aplique combinaciones de teclas solo localmente en el equipo cliente.

</dd> <dt>

1
</dt> <dd>

Aplique combinaciones de teclas en el servidor remoto.

</dd> <dt>

2
</dt> <dd>

Aplique combinaciones de teclas al servidor remoto solo cuando el cliente se ejecute en modo de pantalla completa. Este es el valor predeterminado.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Estas propiedades no se pueden establecer cuando el control está conectado.

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





