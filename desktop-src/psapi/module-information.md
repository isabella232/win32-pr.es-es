---
title: Información de módulos
description: Un módulo es un archivo ejecutable o DLL.
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420821"
---
# <a name="module-information"></a>Información de módulos

Un *módulo* es un archivo ejecutable o dll. Cada proceso está compuesto por uno o más módulos. Puede recuperar la lista de identificadores de módulo para un proceso llamando a la función [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) . Esta función rellena una matriz de valores de **HMODULE** con los identificadores de módulo para el proceso especificado. El primer módulo es el archivo ejecutable. Recuerde que estos identificadores de módulo son más probables de otro proceso, por lo que no puede usarlos con funciones como [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea). Sin embargo, puede usar [las funciones de psapi](psapi-functions.md) para obtener información sobre un módulo de otro proceso.

En el procedimiento siguiente se describe cómo obtener información del módulo de otro proceso.

**Para obtener información del módulo de otro proceso**

1.  Llame a la función [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) . Esta función toma un identificador de proceso y un identificador de módulo como entrada y rellena un búfer con el nombre base de un módulo (por ejemplo, Kernel32.dll). Una función relacionada, [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa), toma los mismos parámetros que la entrada, pero devuelve la ruta de acceso completa al módulo (por ejemplo, C: \\ Windows \\ system32 \\Kernel32.dll).
2.  Llame a la función [**GetModuleInformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) . Esta función toma un identificador de proceso y un identificador de módulo, y rellena una estructura [**MODULEINFO**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) con la dirección de carga del módulo, el tamaño del espacio de direcciones lineal que ocupa y un puntero a su punto de entrada.

Si una aplicación requiere información del módulo para el proceso actual, debe usar la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) en lugar de las funciones del módulo psapi. Esto ayuda al rendimiento de las aplicaciones de dos maneras: la función **GetModuleFileName** es más eficaz que las funciones del módulo psapi y una aplicación puede evitar la carga de psapi.dll si no usa ninguna función de psapi.

Las funciones [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) y [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) se han diseñado principalmente para su uso por parte de depuradores y aplicaciones similares que deben extraer información de módulos de otro proceso. Si la lista de módulos del proceso de destino está dañada o aún no se ha inicializado, o si la lista de módulos cambia durante la llamada de función como resultado de la carga o descarga de los archivos dll, es posible que estas funciones generen errores o devuelvan información incorrecta.

 

 