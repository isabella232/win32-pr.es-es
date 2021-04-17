---
description: Libera los cargadores de clase de Java que se pueden haber consumido al examinar las applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670812"
---
# <a name="notifybrowsershutdown-function"></a>NotifyBrowserShutdown función)

Libera los cargadores de clase de Java que se pueden haber consumido al examinar las applets.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpvReserved* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**. De lo contrario, el valor devuelto es un código de error.

## <a name="remarks"></a>Observaciones

Cuando el recuento de ventanas del explorador llega a cero en el modo Web integrado, esta función libera los cargadores de la clase Java. Cuando el usuario empiece a examinar de nuevo las applets, la máquina virtual de Java descargará los archivos de clase más recientes.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
