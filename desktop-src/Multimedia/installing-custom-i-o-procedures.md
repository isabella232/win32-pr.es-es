---
title: Instalación de procedimientos de e/s personalizados
description: Instalación de procedimientos de e/s personalizados
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de archivos multimedia, procedimientos personalizados
- e/s de archivos, procedimientos personalizados
- entrada y salida (e/s), procedimientos personalizados
- E/s (entrada y salida), procedimientos personalizados
- instalación de procedimientos de e/s personalizados
- e/s personalizada
- mmioInstallIOProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420704"
---
# <a name="installing-custom-io-procedures"></a>Instalación de procedimientos de e/s personalizados

Para instalar un procedimiento de e/s asociado a. Extensión de nombre de archivo ARC, use la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) de la siguiente manera:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Al instalar un procedimiento de e/s mediante [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), el procedimiento permanece instalado hasta que lo quite. El procedimiento de e/s se usa para cualquier archivo que se abra siempre que el archivo tenga la extensión de nombre de archivo adecuada.

También puede instalar temporalmente un procedimiento de e/s mediante la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . En este caso, el procedimiento de e/s se usa solo con un archivo abierto mediante **mmioOpen** y se quita cuando se cierra el archivo mediante la función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) . Para especificar un procedimiento de e/s al abrir un archivo con **mmioOpen**, use el parámetro *lpmmioinfo* para hacer referencia a una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) de la siguiente manera:

1.  Establezca el miembro **fccIOProc** en **null**.
2.  Establezca el miembro **pIOProc** en la dirección de instancia de procedimiento del procedimiento de e/s.
3.  Establezca el resto de miembros en cero (a menos que esté abriendo un archivo de memoria o leyendo o escribiendo directamente en el búfer de e/s de archivo).

Asegúrese de quitar los procedimientos de e/s que haya instalado antes de salir de la aplicación.

 

 