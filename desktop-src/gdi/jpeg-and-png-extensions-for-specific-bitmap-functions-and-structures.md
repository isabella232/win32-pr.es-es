---
description: En determinadas versiones de Microsoft Windows, las funciones StretchDIBits y SetDIBitsToDevice permiten pasar imágenes JPEG y PNG como imagen de origen a los dispositivos de impresora.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115295"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas

En determinadas versiones de Microsoft Windows, las funciones [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) y [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) permiten pasar imágenes JPEG y PNG como imagen de origen a los dispositivos de impresora. Esta extensión no está pensada como un medio para proporcionar descompresión general de JPEG y PNG a las aplicaciones, sino que permite a las aplicaciones enviar imágenes comprimidas con JPEG y PNG directamente a impresoras que admiten hardware para imágenes JPEG y PNG.

Las estructuras [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) y [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) se extienden para permitir la especificación de valores **de biCompression** que indican que los datos de mapa de bits son una imagen JPEG o PNG. Estos valores de compresión solo son válidos para [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) y [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) cuando el *parámetro hdc* especifica un dispositivo de impresora. Para admitir la cola de metarchivos de la impresora, la aplicación no debe confiar en el valor devuelto para determinar si el dispositivo admite el archivo JPEG o PNG. La aplicación debe emitir QUERYESCSUPPORT con el escape correspondiente antes de llamar a **SetDIBitsToDevice** y **StretchDIBits**. Si se produce un error en el escape de validación, la aplicación debe volver a usar su propia compatibilidad con JPEG o PNG para descomprimir la imagen en un mapa de bits.

 

 
