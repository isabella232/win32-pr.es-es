---
description: Conversión manual desde MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversión manual desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d384a6ca5f6afa2d0563249c78e1120349e28e053f1cad923a6ae2bdcdb8849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070565"
---
# <a name="manual-conversion-from-mts"></a>Conversión manual desde MTS

Es posible que quiera aislar la conversión de paquetes MTS en aplicaciones COM+ para que esté fuera del proceso de Windows de instalación. El procedimiento siguiente ofrece un enfoque alternativo:

1.  Exporte los paquetes MTS mediante la característica de exportación de paquetes MTS 2.0 (lo que da como resultado un archivo de paquete MTS y una colección de otros archivos).
2.  Elimine los paquetes MTS y actualice Windows, o realice una instalación limpia de Windows.
3.  Instale los archivos del paquete MTS (.pack) en un sistema Windows 2000 o posterior mediante el Asistente para instalación de aplicaciones de la herramienta administrativa servicios de componentes. También deberá restablecer la identidad "Ejecutar como" de la aplicación en el registro del sistema en **HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ APPID \\ RunAs**.

> [!Note]  
> Solo el procedimiento de conversión automática (mediante Windows o mediante la ejecución de la utilidad MTSTOCOM) genera el archivo de registro MTSTOCOM. Este archivo no se genera al seguir el procedimiento de conversión manual.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión automática desde MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados y problemas de conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



