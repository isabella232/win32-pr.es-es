---
title: Instalación de procedimientos de E/S personalizados
description: Instalación de procedimientos de E/S personalizados
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- E/S de archivos multimedia, procedimientos personalizados
- E/S de archivo, procedimientos personalizados
- entrada y salida (E/S), procedimientos personalizados
- E/S (entrada y salida),procedimientos personalizados
- instalación de procedimientos de E/S personalizados
- E/S personalizada
- Función mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371815"
---
# <a name="installing-custom-io-procedures"></a>Instalación de procedimientos de E/S personalizados

Para instalar un procedimiento de E/S asociado a . Extensión de nombre de archivo de ARC, use [**la función mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) como se muestra a continuación:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Cuando se instala un procedimiento de E/S mediante [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), el procedimiento permanece instalado hasta que se quita. El procedimiento de E/S se usa para cualquier archivo que abra, siempre que el archivo tenga la extensión de nombre de archivo adecuada.

También puede instalar temporalmente un procedimiento de E/S mediante la [**función mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) En este caso, el procedimiento de E/S solo se usa con un archivo abierto mediante **mmioOpen** y se quita cuando el archivo se cierra mediante la [**función mmioClose.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) Para especificar un procedimiento de E/S al abrir un archivo mediante **mmioOpen**, use el parámetro *lpmmioinfo* para hacer referencia a una [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) como se muestra a continuación:

1.  Establezca el **miembro fccIOProc** en **NULL.**
2.  Establezca el **miembro pIOProc** en la dirección de instancia de procedimiento del procedimiento de E/S.
3.  Establezca todos los demás miembros en cero (a menos que abra un archivo de memoria o lea o escriba directamente en el búfer de E/S de archivo).

Asegúrese de quitar los procedimientos de E/S que haya instalado antes de salir de la aplicación.

 

 