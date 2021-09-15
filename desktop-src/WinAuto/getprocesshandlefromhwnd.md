---
title: Función GetProcessHandleFromHwnd
description: Recupera un identificador de proceso de un identificador de ventana.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Función GetProcessHandleFromHwnd Windows accesibilidad
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568541"
---
# <a name="getprocesshandlefromhwnd-function"></a>Función GetProcessHandleFromHwnd

Recupera un identificador de proceso de un identificador de ventana.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Identificador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HANDLE**](/windows/desktop/WinProg/windows-data-types)**

Si se realiza correctamente, devuelve el identificador del proceso que posee la ventana.

Si no se realiza correctamente, devuelve **NULL.**

## <a name="remarks"></a>Observaciones

En versiones anteriores del sistema operativo, un proceso podía abrir otro proceso (para acceder a su memoria, por ejemplo) mediante [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Esta función se realiza correctamente si el autor de la llamada tiene los privilegios adecuados; normalmente, el llamador y el proceso de destino deben ser el mismo usuario.

En Windows Vista, sin embargo, Se produce un error [**en OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) en el escenario en el que el autor de la llamada tiene UIAccess y el proceso de destino se eleva. En este caso, el propietario del proceso de destino está en el grupo Administradores, pero el proceso de llamada se ejecuta con el token restringido, por lo que no tiene pertenencia a este grupo y se le deniega el acceso al proceso con privilegios elevados. Sin embargo, si el autor de la llamada tiene UIAccess, puede usar un enlace de Windows para insertar código en el proceso de destino y, desde dentro del proceso de destino, enviar un identificador al autor de la llamada.

**GetProcessHandleFromHwnd es** una función útil que usa esta técnica para obtener el identificador del proceso que posee el HWND especificado. Tenga en cuenta que solo se realiza correctamente en los casos en los que el llamador y el proceso de destino se ejecutan como el mismo usuario. El identificador devuelto tiene los siguientes privilegios: PROCESS \_ DUP \_ HANDLE PROCESS VM OPERATION PROCESS VM READ PROCESS VM \| WRITE \_ \_ \| \_ \_ \| \_ \_ \| SYNCHRONIZE. Si se requieren otros privilegios, puede que sea necesario implementar la técnica de enlace explícitamente en lugar de usar esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

