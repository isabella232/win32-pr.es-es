---
title: Servicios personalizados
description: Servicios personalizados
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- E/S de archivos multimedia, servicios personalizados
- E/S de archivo, servicios personalizados
- entrada y salida (E/S), servicios personalizados
- E/S (entrada y salida), servicios personalizados
- E/S personalizada
- Función mmioInstallIOProc
- Función mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372152"
---
# <a name="custom-services"></a>Servicios personalizados

Los servicios de E/S de archivos multimedia usan procedimientos de E/S para controlar la entrada y salida física asociadas a la lectura y escritura en diferentes tipos de sistemas de almacenamiento, como sistemas de archivo y sistemas de almacenamiento de base de datos. Existen procedimientos de E/S predefinidos para los sistemas de archivos estándar y para los archivos de memoria, pero puede proporcionar un procedimiento de E/S personalizado para acceder a un sistema de almacenamiento único mediante la función [**mmioInstallIOProc.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)

Para abrir un archivo mediante un procedimiento de E/S personalizado, use la [**función mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Incluya un signo más (+) o la constante CFSEPCHAR en el nombre de archivo para separar el nombre del archivo físico del nombre del elemento del archivo que desea abrir. En el ejemplo siguiente se abre un elemento de archivo denominado "element" desde un archivo denominado FILENAME. ARCO:


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Cuando el administrador de E/S de archivos encuentra un signo más en un nombre de archivo, examina la extensión de nombre de archivo para determinar qué procedimiento de E/S se va a asociar al archivo. En el ejemplo anterior, el administrador de E/S de archivos intentaría usar el procedimiento de E/S asociado a . Extensión de nombre de archivo de ARC; Este procedimiento de E/S se habría instalado mediante [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Si no hay ningún procedimiento de E/S instalado, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) devuelve un error.

Los procedimientos de E/S deben responder a los mensajes siguientes:

-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**MMIOM \_ SEEK**](mmiom-seek.md)
-   [**CAMBIO DE NOMBRE DE MMIOM \_**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

También puede crear mensajes personalizados y enviarlos al procedimiento de E/S mediante la [**función mmioSendMessage.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) Si define sus propios mensajes, asegúrese de que están definidos en o por encima del valor definido por la constante \_ USER de MMIOM.

Además de procesar mensajes, un procedimiento de E/S debe mantener el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (al que apunta el parámetro *lpmmioinfo* de la **función mmioOpen).** El **miembro lDiskOffset** siempre debe contener el desplazamiento de archivo a la ubicación a la que accederá el siguiente mensaje \_ MMIOM READ o MMIOM \_ WRITE. El desplazamiento se especifica en bytes y es relativo al principio del archivo. El procedimiento de E/S puede usar el **miembro adwInfo** para mantener cualquier información de estado necesaria. El procedimiento de E/S no debe modificar ningún otro miembro de la **estructura MMIOINFO.**

 

 