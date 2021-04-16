---
description: La función ShowJavaConsole es una ayuda para la depuración para los desarrolladores de Java. Las applets (u otro código Java) que se ejecutan en Internet Explorer pueden usarla para mostrar mensajes de error y otra información.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649827"
---
# <a name="showjavaconsole-function"></a>ShowJavaConsole función)

La función **ShowJavaConsole** es una ayuda para la depuración para los desarrolladores de Java. Las applets (u otro código Java) que se ejecutan en Internet Explorer pueden usarla para mostrar mensajes de error y otra información.

## <a name="syntax"></a>Sintaxis


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

<dl></dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La llamada a **ShowJavaConsole** hace que la máquina virtual Java muestre la ventana de la consola Java. La propia ventana de la consola Java puede mostrar la salida de depuración del código Java que se ejecuta en el proceso de llamada. Normalmente, solo lo usaría una aplicación que hospeda la máquina virtual Java. Solo hay una ventana de consola de Java por cada proceso. varias llamadas a la API provocan que se muestre la misma ventana. En otras palabras, si ya se muestra la ventana de la consola, no sucede nada; Si la ventana no se ha mostrado o el usuario la ha cerrado, se abrirá la ventana.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
