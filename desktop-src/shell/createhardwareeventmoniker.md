---
description: Crea un moniker que representa un componente de hardware y su controlador de eventos asociado. AutoPlay usa esta función para permitir que las aplicaciones usen eventos de Reproducción automática.
title: Función CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468274"
---
# <a name="createhardwareeventmoniker-function"></a>Función CreateHardwareEventMoniker

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Crea un moniker que representa un componente de hardware y su controlador de eventos asociado. AutoPlay usa esta función para permitir que las aplicaciones usen eventos de Reproducción automática.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clsid* \[ En\]
</dt> <dd>

Tipo: **REFCLSID**

Identificador de la clase a la que se enlaza el moniker.

</dd> <dt>

*pszEventHandler* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Nombre del controlador de eventos.

</dd> <dt>

*ppmoniker* \[ out\]
</dt> <dd>

Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Dirección de una variable de puntero que recibe el [**puntero de interfaz IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Use **CreateHardwareEventMoniker al** registrar aplicaciones en ejecución para que esas aplicaciones tengan acceso a eventos de Reproducción automática. Para usar eventos de Reproducción automática en aplicaciones en ejecución, primero debe crear un nuevo componente que implemente la [**interfaz IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) Inicialice esta interfaz con el valor InitCmdLine de la entrada del controlador en particular bajo la clave **Handlers,** porque AutoPlay no llama al [**método Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize)

Debe llamar a **CreateHardwareEventMoniker para** obtener un moniker que represente el componente y su controlador de eventos. A continuación, use el valor devuelto en el parámetro *ppmoniker* para registrar el componente en la tabla de objetos en ejecución (ROT), como se muestra en el ejemplo.

Tenga en **cuenta que CreateHardwareEventMoniker** no está definido en un archivo de encabezado. Para usarlo en el código, debe obtener un identificador para el archivo Shsvcs.dll mediante una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). A continuación, use ese identificador en una llamada a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener una instancia de la **función CreateHardwareEventMoniker.**

La llamada a [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiere que escriba la **siguiente información de AppID** en el Registro.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ninguna</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
