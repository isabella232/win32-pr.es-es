---
title: GetProcessHandleFromHwnd función)
description: Recupera un identificador de proceso de un identificador de ventana.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Función GetProcessHandleFromHwnd accesibilidad de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150332"
---
# <a name="getprocesshandlefromhwnd-function"></a>GetProcessHandleFromHwnd función)

Recupera un identificador de proceso de un identificador de ventana.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Tipo: **[ **hWnd**](/windows/desktop/WinProg/windows-data-types)**

Identificador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **Handle**](/windows/desktop/WinProg/windows-data-types)**

Si es correcto, devuelve el identificador del proceso que posee la ventana.

Si no se realiza correctamente, devuelve **null**.

## <a name="remarks"></a>Observaciones

En versiones anteriores del sistema operativo, un proceso podía abrir otro proceso (para tener acceso a su memoria, por ejemplo) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Esta función se ejecuta correctamente si el autor de la llamada tiene los privilegios adecuados; Normalmente, el llamador y el proceso de destino deben ser el mismo usuario.

En Windows Vista, sin embargo, se produce un error de [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) en el escenario en el que el llamador tiene UIAccess y el proceso de destino se eleva. En este caso, el propietario del proceso de destino se encuentra en el grupo administradores, pero el proceso de llamada se ejecuta con el token restringido, por lo que no es miembro de este grupo y se le deniega el acceso al proceso elevado. Sin embargo, si el autor de la llamada tiene UIAccess, puede usar un enlace de Windows para insertar código en el proceso de destino y, desde dentro del proceso de destino, devolver un identificador al autor de la llamada.

**GetProcessHandleFromHwnd** es una función útil que utiliza esta técnica para obtener el identificador del proceso que posee el HWND especificado. Tenga en cuenta que solo se realiza correctamente en los casos en los que el llamador y el proceso de destino se ejecutan como el mismo usuario. El identificador devuelto tiene los siguientes privilegios: procesar identificador de proceso de máquina virtual proceso de operación de VM lectura de máquina virtual \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ escritura \| sincronizar. Si se requieren otros privilegios, es posible que sea necesario implementar la técnica de enlace explícitamente en lugar de utilizar esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

