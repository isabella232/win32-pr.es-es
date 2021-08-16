---
description: Instala un nuevo dispositivo. Se pide al usuario que seleccione el dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Función InstallNewDevice
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
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405317"
---
# <a name="installnewdevice-function"></a>Función InstallNewDevice

Instala un nuevo dispositivo. Se pide al usuario que seleccione el dispositivo.

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

*hwndParent* \[ En\]
</dt> <dd>

Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.

</dd> <dt>

*ClassGuid* \[ En\]
</dt> <dd>

Puntero a un **GUID de clase.** Este parámetro es opcional. Si este parámetro es **NULL,** el usuario comienza en la página de opción de detección. Si este parámetro es **GUID \_ NULL o** GUID **\_ DEVCLASS \_ UNKNOWN,** el usuario comienza en la página de selección de clases.

</dd> <dt>

*pReboot* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el estado de reinicio. Este parámetro puede ser **DI \_ NEEDRESTART** o **DI \_ NEEDREBOOT.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a NewDev.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                        |
| Archivo DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administración de dispositivos functions](device-management-functions.md)
</dt> </dl>

 

