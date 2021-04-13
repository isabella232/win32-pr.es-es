---
title: Run-Time vincular a Wtsapi32.dll
description: La aplicación puede usar la API de Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la función LoadLibrary para cargar Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421107"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time vincular a Wtsapi32.dll

Si la aplicación se ejecuta en un entorno que no es un Servicios de Escritorio remoto entorno, pero desea que la aplicación proporcione funcionalidad adicional cuando se ejecuta en un entorno de Servicios de Escritorio remoto, la aplicación puede usar la API de Servicios de Escritorio remoto para implementar la funcionalidad adicional y vincular dinámicamente a la Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll. Si se produce un error en la llamada **LoadLibrary** , la aplicación se puede ejecutar utilizando su funcionalidad básica. Si **LoadLibrary** se ejecuta correctamente, la aplicación puede llamar a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar punteros a las funciones servicios de escritorio remoto a las que desea llamar.

Si la aplicación está destinada solo a un entorno de Servicios de Escritorio remoto, la vinculación dinámica no es necesaria. En este caso, puede incluir Wtsapi32. h y vincular con Wtsapi32. lib. Después, si la aplicación se inicia en un entorno que no sea Servicios de Escritorio remoto, se cerrará porque Wtsapi32.dll no está presente.

Para obtener información acerca de cómo determinar si la aplicación se ejecuta en un entorno de Servicios de Escritorio remoto, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones generales de programación](general-programming-guidelines.md)
</dt> </dl>

 

 