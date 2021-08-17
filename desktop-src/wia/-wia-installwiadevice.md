---
description: La función InstallWiaDevice instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo enumerado en la raíz. Puede aparecer una advertencia de seguridad si algún archivo de instalación o coinstalador no está firmado digitalmente y es de confianza.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Función InstallWiaDevice (Wia.h)
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
ms.openlocfilehash: 10006e234c9a76054a77fb64f89a31d9a21e394066bcc98813912bad9f804e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965844"
---
# <a name="installwiadevice-function"></a>Función InstallWiaDevice

La **función InstallWiaDevice** instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo enumerado en la raíz. Puede aparecer una advertencia de seguridad si algún archivo de instalación o coinstalador no está firmado digitalmente y es de confianza.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaDeviceInstall* \[ En\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \***

Puntero a una estructura WIADEVICEINSTALL. El *miembro szFriendlyName* de la estructura debe establecerse en el dispositivo FriendlyName real.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, devuelve un código de error de Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




