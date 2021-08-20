---
description: Libera los cargadores de clases de Java que se pueden haber consumido al examinar los applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Función NotifyBrowserShutdown
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
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826821"
---
# <a name="notifybrowsershutdown-function"></a>Función NotifyBrowserShutdown

Libera los cargadores de clases de Java que se pueden haber consumido al examinar los applets.

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

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**. De lo contrario, el valor devuelto es un código de error.

## <a name="remarks"></a>Comentarios

Cuando el recuento de ventanas del explorador alcanza cero en modo web integrado, esta función libera los cargadores de clases de Java. Cuando el usuario empiece a examinar applets de nuevo, la máquina virtual Java descargará los archivos de clase más recientes.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
