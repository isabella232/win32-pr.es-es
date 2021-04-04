---
description: La función InstallWiaDevice instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo raíz enumerado. Puede mostrar una advertencia de seguridad si algún archivo o Coinstalador de instalación no está firmado digitalmente y es de confianza.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Función InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810796"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice función)

La función **InstallWiaDevice** instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo raíz enumerado. Puede mostrar una advertencia de seguridad si algún archivo o Coinstalador de instalación no está firmado digitalmente y es de confianza.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaDeviceInstall* \[ de\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \** _

Puntero a una estructura WIADEVICEINSTALL. El miembro _szFriendlyName * de la estructura se debe establecer en el dispositivo FriendlyName real.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, devuelve un código de error de Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




