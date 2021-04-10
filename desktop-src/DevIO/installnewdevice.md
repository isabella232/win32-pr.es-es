---
description: Instala un nuevo dispositivo. Se solicita al usuario que seleccione el dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153332"
---
# <a name="installnewdevice-function"></a>InstallNewDevice función)

Instala un nuevo dispositivo. Se solicita al usuario que seleccione el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.

</dd> <dt>

*ClassGuid* \[ de\]
</dt> <dd>

Un puntero a un **GUID** de clase. Este parámetro es opcional. Si este parámetro es **null**, el usuario se inicia en la página de opciones de detección. Si este parámetro es **GUID \_ null** o **GUID \_ DEVCLASS \_ Unknown**, el usuario se inicia en la página de selección de clases.

</dd> <dt>

*Inicio previo* \[ enuncia\]
</dt> <dd>

Un puntero a una variable que recibe el estado de reinicio. Este parámetro puede ser **di \_ NEEDRESTART** o **di \_ NEEDREBOOT**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a NewDev.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                        |
| Archivo DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de administración de dispositivos](device-management-functions.md)
</dt> </dl>

 

