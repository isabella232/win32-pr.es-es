---
description: En determinadas versiones de Microsoft Windows, las funciones StretchDIBits y SetDIBitsToDevice permiten pasar imágenes JPEG y PNG como imagen de origen a dispositivos de impresora.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625dcde0e673c85dcaef65c2f1aa825121bf871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544454"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas

En determinadas versiones de Microsoft Windows, las funciones [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) y [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) permiten pasar imágenes JPEG y PNG como imagen de origen a dispositivos de impresora. Esta extensión no está pensada como un medio para proporcionar descompresión general JPEG y PNG a las aplicaciones, sino que permite que las aplicaciones envíen imágenes comprimidas JPEG y PNG directamente a las impresoras que tienen compatibilidad de hardware con imágenes JPEG y PNG.

Las estructuras [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) y [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) se extienden para permitir la especificación de valores de **bicompresión** que indican que los datos de mapa de bits son imágenes JPEG o PNG. Estos valores de compresión solo son válidos para [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) y [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) cuando el parámetro *HDC* especifica un dispositivo de impresora. Para admitir la puesta en cola de metarchivos de la impresora, la aplicación no debe basarse en el valor devuelto para determinar si el dispositivo admite el archivo JPEG o PNG. La aplicación debe emitir QUERYESCSUPPORT con el escape correspondiente antes de llamar a **SetDIBitsToDevice** y **StretchDIBits**. Si se produce un error en la conmutación por error de validación, la aplicación debe revertir a su propia compatibilidad con JPEG o PNG para descomprimir la imagen en un mapa de bits.

 

 
