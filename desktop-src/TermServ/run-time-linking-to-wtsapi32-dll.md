---
title: Run-Time vinculación a Wtsapi32.dll
description: La aplicación puede usar la API Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la función LoadLibrary para cargar Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc686f26029ee9bfa4332215e27a587a7e57b78de9bd0d1043ee58541ef76194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127500"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time vinculación a Wtsapi32.dll

Si la aplicación se ejecuta en un entorno que no es un entorno de Servicios de Escritorio remoto, pero desea que la aplicación proporcione funcionalidad adicional cuando se ejecuta en un entorno de Servicios de Escritorio remoto, la aplicación puede usar la API de Servicios de Escritorio remoto para implementar la funcionalidad adicional y vincular dinámicamente a Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la [**función LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll. Si se produce un error en la llamada **LoadLibrary,** la aplicación puede ejecutarse con su funcionalidad básica. Si **LoadLibrary** se realiza correctamente, la aplicación puede llamar a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar punteros a Servicios de Escritorio remoto funciones a las que desea llamar.

Si la aplicación está pensada solo para un entorno Servicios de Escritorio remoto, no es necesaria la vinculación dinámica. En este caso, puede incluir Wtsapi32.h y un vínculo con Wtsapi32.lib. A continuación, si la aplicación se inicia en un entorno distinto de Servicios de Escritorio remoto, se cerrará porque Wtsapi32.dll no está presente.

Para obtener información sobre cómo determinar si la aplicación se está ejecutando en un entorno Servicios de Escritorio remoto, vea [Detección](detecting-the-terminal-services-environment.md)del Servicios de Escritorio remoto virtual .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices generales de programación](general-programming-guidelines.md)
</dt> </dl>

 

 