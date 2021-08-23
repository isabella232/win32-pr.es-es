---
description: La función ShowJavaConsole es una ayuda de depuración para desarrolladores de Java. Los applets (u otro código Java) que se ejecutan Internet Explorer pueden usarlos para mostrar mensajes de error y otra información.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Función ShowJavaConsole
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
ms.openlocfilehash: 0a8517d32057b6434d3822cc02977f6afd72c1b387b78e85e53810bd27f00550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075859"
---
# <a name="showjavaconsole-function"></a>Función ShowJavaConsole

La **función ShowJavaConsole** es una ayuda de depuración para desarrolladores de Java. Los applets (u otro código Java) que se ejecutan Internet Explorer pueden usarlos para mostrar mensajes de error y otra información.

## <a name="syntax"></a>Sintaxis


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

<dl></dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al **llamar a ShowJavaConsole,** la máquina virtual Java muestra la ventana de la consola de Java. La propia ventana de consola de Java puede mostrar la salida de depuración del código Java que se ejecuta en el proceso de llamada. Normalmente, solo lo usaría una aplicación que hospeda la máquina virtual Java. Solo hay una ventana de consola de Java por proceso; Varias llamadas a la API darán como resultado la misma ventana que se muestra. En otras palabras, si ya se muestra la ventana de consola, no ocurre nada; Si no se ha mostrado la ventana o el usuario la ha cerrado, aparece la ventana.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
