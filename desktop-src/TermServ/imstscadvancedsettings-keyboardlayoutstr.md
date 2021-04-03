---
title: Propiedad KeyBoardLayoutStr de IMsTscAdvancedSettings
description: Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado distribución del teclado) que se va a usar para la conexión.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad KeyBoardLayoutStr
- Propiedad KeyBoardLayoutStr Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad KeyBoardLayoutStr
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
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802276"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>IMsTscAdvancedSettings:: KeyBoardLayoutStr (propiedad)

Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado distribución del teclado) que se va a usar para la conexión.

Si no se establece esta propiedad, el control utiliza el diseño predeterminado devuelto por la función [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .

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

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

La propiedad es un número hexadecimal de ocho dígitos en forma de cadena. Los cuatro dígitos inferiores representan el identificador de idioma y los cuatro dígitos superiores representan la variación del teclado dentro de ese idioma. Por lo tanto, por ejemplo, "00000409" representaría el teclado inglés de EE. UU. predeterminado porque "0409" es el identificador de idioma Inglés de EE. UU. La variación Dvorak del teclado inglés de EE. UU. tiene un identificador de "00010409". Puede encontrar las distribuciones de teclado disponibles, enumeradas por los identificadores de distribución de teclado, en el registro en

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

