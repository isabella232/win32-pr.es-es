---
title: Servicios personalizados
description: Servicios personalizados
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de archivos multimedia, servicios personalizados
- e/s de archivos, servicios personalizados
- entrada y salida (e/s), servicios personalizados
- E/s (entrada y salida), servicios personalizados
- e/s personalizada
- mmioInstallIOProc función)
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077705"
---
# <a name="custom-services"></a>Servicios personalizados

Los servicios de e/s de archivos multimedia usan procedimientos de e/s para controlar la entrada y la salida física asociadas a la lectura y la escritura en diferentes tipos de sistemas de almacenamiento, como sistemas de archivo de archivos y sistemas de almacenamiento de base de datos. Existen procedimientos de e/s predefinidos para los sistemas de archivos estándar y para los archivos de memoria, pero puede proporcionar un procedimiento de e/s personalizado para tener acceso a un sistema de almacenamiento único mediante la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .

Para abrir un archivo mediante un procedimiento de e/s personalizado, use la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Incluya un signo más (+) o la constante CFSEPCHAR en el nombre de archivo para separar el nombre del archivo físico del nombre del elemento del archivo que desea abrir. En el ejemplo siguiente se abre un elemento de archivo denominado "Element" desde un archivo denominado FILENAME. VERÍA


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Cuando el administrador de e/s de archivos encuentra un signo más en un nombre de archivo, examina la extensión del nombre de archivo para determinar el procedimiento de e/s que se va a asociar al archivo. En el ejemplo anterior, el administrador de e/s de archivos intentaría usar el procedimiento de e/s asociado a. Extensión de nombre de archivo ARC; Este procedimiento de e/s se habría instalado con [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Si no hay ningún procedimiento de e/s instalado, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) devuelve un error.

Los procedimientos de e/s deben responder a los siguientes mensajes:

-   [**MMIOM \_ cerrar**](mmiom-close.md)
-   [**MMIOM \_ abrir**](mmiom-open.md)
-   [**MMIOM \_ lectura**](mmiom-read.md)
-   [**escritura de MMIOM \_**](mmiom-write.md)
-   [**búsqueda de MMIOM \_**](mmiom-seek.md)
-   [**MMIOM \_ cambiar nombre**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

También puede crear mensajes personalizados y enviarlos al procedimiento de e/s mediante la función [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) . Si define sus propios mensajes, asegúrese de que están definidos en o por encima del valor definido por la \_ constante de usuario MMIOM.

Además de procesar mensajes, un procedimiento de e/s debe mantener el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (al que apunta el parámetro *lpmmioinfo* de la función **mmioOpen** ). El miembro **lDiskOffset** debe contener siempre el desplazamiento de archivo en la ubicación a la que tendrá acceso el siguiente MMIOM de \_ lectura o MMIOM escritura de \_ . El desplazamiento se especifica en bytes y es relativo al principio del archivo. El procedimiento de e/s puede usar el miembro **adwInfo** para mantener la información de estado necesaria. El procedimiento de e/s no debe modificar ningún otro miembro de la estructura **MMIOINFO** .

 

 