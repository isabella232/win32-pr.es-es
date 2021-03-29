---
description: Crea un moniker que representa un componente de hardware y su controlador de eventos asociado. La reproducción automática usa esta función para permitir que las aplicaciones usen eventos de reproducción automática.
title: CreateHardwareEventMoniker función)
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
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984327"
---
# <a name="createhardwareeventmoniker-function"></a>CreateHardwareEventMoniker función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Crea un moniker que representa un componente de hardware y su controlador de eventos asociado. La reproducción automática usa esta función para permitir que las aplicaciones usen eventos de reproducción automática.

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

*CLSID* \[ de de\]
</dt> <dd>

Tipo: **REFCLSID**

IDENTIFICADOR de la clase a la que se enlaza el moniker.

</dd> <dt>

*pszEventHandler* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Nombre del controlador de eventos.

</dd> <dt>

*ppmoniker* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Dirección de una variable de puntero que recibe el puntero de interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use **CreateHardwareEventMoniker** al registrar aplicaciones en ejecución para que dichas aplicaciones tengan acceso a los eventos de reproducción automática. Para usar eventos de reproducción automática en aplicaciones en ejecución, primero debe crear un nuevo componente que implemente la interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) . Inicialice esta interfaz con el valor InitCmdLine de la entrada del controlador en cuestión bajo la clave **handlers** , ya que la reproducción automática no llama al método [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .

Debe llamar a **CreateHardwareEventMoniker** para obtener un moniker que represente el componente y su controlador de eventos. A continuación, use el valor devuelto en el parámetro *ppmoniker* para registrar su componente en la tabla de objetos en ejecución (Rot) como se muestra en el ejemplo.

Tenga en cuenta que **CreateHardwareEventMoniker** no está definido en un archivo de encabezado. Para usarlo en el código, debe obtener un identificador para el Shsvcs.dll archivo a través de una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). A continuación, use ese controlador en una llamada a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener una instancia de la función **CreateHardwareEventMoniker** .

La llamada a [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiere que escriba la siguiente información de **AppID** en el registro.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
