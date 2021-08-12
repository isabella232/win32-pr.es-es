---
title: Propiedad IMsTscAdvancedSettings KeyBoardLayoutStr
description: Especifica el nombre del identificador de configuración regional de entrada activa (anteriormente denominado diseño de teclado) que se usará para la conexión.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Propiedad KeyBoardLayoutStr Servicios de Escritorio remoto
- Propiedad KeyBoardLayoutStr Servicios de Escritorio remoto , interfaz IMsTscAdvancedSettings
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto , propiedad KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c87cb55b22658f704b328a51435ca2554d4c6574e25484253f9899475918642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606182"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Propiedad IMsTscAdvancedSettings::KeyBoardLayoutStr

Especifica el nombre del identificador de configuración regional de entrada activa (anteriormente denominado diseño de teclado) que se usará para la conexión.

Si no se establece esta propiedad, el control usa el diseño predeterminado devuelto por la [**función GetKeyboardLayout.**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout)

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del identificador de configuración regional de entrada activo.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

La propiedad es un número hexadecimal de ocho dígitos en forma de cadena. Los cuatro dígitos inferiores representan el identificador de idioma y los cuatro dígitos superiores representan la variación del teclado dentro de ese idioma. Por ejemplo, "00000409" representaría el teclado en inglés de EE. UU. predeterminado porque "0409" es el identificador del idioma inglés de ESTADOS UNIDOS. La variación DeAk del teclado inglés de Estados Unidos tiene un identificador de "00010409". Puede encontrar los diseños de teclado disponibles, enumerados por sus identificadores de diseño de teclado, en el Registro en

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

