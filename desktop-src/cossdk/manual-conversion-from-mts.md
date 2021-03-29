---
description: Conversión manual desde MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversión manual desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807375"
---
# <a name="manual-conversion-from-mts"></a>Conversión manual desde MTS

Es posible que desee aislar la conversión de paquetes MTS en aplicaciones COM+ para que quede fuera del proceso de instalación de Windows. El siguiente procedimiento ofrece un enfoque alternativo:

1.  Exporte los paquetes MTS mediante la característica de exportación de paquetes MTS 2,0 (lo que da como resultado un archivo de paquete MTS y una colección de otros archivos).
2.  Elimine los paquetes MTS y actualice Windows, o realice una instalación limpia de Windows.
3.  Instale los archivos de paquete MTS (. Pak) en un sistema Windows 2000 o posterior mediante el Asistente para instalación de aplicaciones de la herramienta administrativa Servicios de componentes. También tendrá que restablecer la identidad "ejecutar como" de la aplicación en el registro del sistema en **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID \\ runas**.

> [!Note]  
> Solo el procedimiento de conversión automática (a través del programa de instalación de Windows o mediante la utilidad MTSTOCOM) genera el archivo de registro MTSTOCOM. Este archivo no se genera al seguir el procedimiento de conversión manual.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión automática desde MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados y problemas de la conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



